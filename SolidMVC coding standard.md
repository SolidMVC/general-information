S.O.L.I.D. MVC CODING STANDARD:
-----------------------------------------------------

From Php-Fig.org "PSR Naming Conventions":
Abstract classes MUST be prefixed by Abstract: e.g. Psr\Foo\AbstractBar.
PSR-1, PSR-2 and PSR-4 MUST be followed.
//////////////////////////////////////////////////////
From PHP.net:
Interfaces are prefixed with "iName" (http://php.net/manual/en/language.oop5.interfaces.php) (in C# language it is 'IName', but in Php we want to have this for easier autoloading and separating-out files that are not classes inside,
i.e. that autoloader will know when to load 'class.InteligentUser.php' and when 'interface.iUser.php')
Traits are prefixed with "tName" (http://php.net/manual/en/language.oop5.traits.php)
//////////////////////////////////////////////////////
0. Global variable and function names naming rules:
0.1. If that is a term, i.e. "ZIP Code", then we use underscore after all-capitals term, i.e.:
	public function getZIP_Code()
	{
		$retZIP_Code = '';
		...
	}
0.2. "yURL" is correct format for variables, not "yUrl".

0.3. Admin HTML lists whose HTML stays in that exact variable, has to be prefixed with '$admin' / '->admin', and suffixed by 'HTML' .
Corresponding class methods must have 'getAdminList' prefix and 'HTML' suffix', i.e.:
<?php
final class TaxesObserver implements ObserverInterface
{
	//<...>
	
	public function getAdminList(...)
	{
		//<...>
	}
}
?>

0.4. All methods and functions that returns HTML, and variables that holds the HTML, should have a suffix 'HTML', i.e.
FOR MODEL: <?php $this->view->greatDropdownOptionsHTML = StaticFormatter::getNumberDropdownOptionsHTML(...); ?>
USAGE INFOR TEMPLATE: <?=$greatDropdownOptionsHTML;?>

0.5. All HTML outputs in templates and model's (for $retHTML) where we DO NOT do comparison, but only ouput, use the esc_url method, i.e.
<?=esc_url($formAction);?>
<?=esc_url($customerAddEditURL);?>

0.6. For JS variables and Classes we should NOT use any dynamic 'prefixed' from PHP, as that makes JS re-factoring/renaming over-complicated in PHPStorm IDE.
As well as the code would get too complicated. If we have multiple extensions, we just uses JS multi-dimensional arrays for that with extension name as array key.
Also do not use $actJS, $popupJS or similar variables for HTML code parameters of Pop-Up JavaScript calls, HTML events ('onclick', 'onchange', etc.), or HTML URL calls to JavaScript.

1. include 'file.php'; - use single ', not do not use brackets for "include" - 'include' is not a function, it's a resource request.

1.1. $objX->specialMethod('specialValue'); - use single ', not "

2. use print(). Do not use echo

3. Make variable local, if that doesn't need to be global (including controller class variables instead of variables accessible only within that specific method) - it confuses less

4. $printVar -> variables is ready for printing to output ONLY (and is escaped by esc_html in controller if that is a string)

5. $var -> variable is used for params, data, input, and is not escaped. Can be printed if that is integer or float.

6. esc_attr(..), esc_textarea(..) for editing data in input or textarea fields for string values must be used in element model with 'edit_' prefix. This is not applied for integer, iso date, iso time, or float values, as they are know formats.

7. The templates should not have the '$printVariable' used anywhere, even if that is coming from print. As it should be defined/managed only by the controller, not by the view, what is used for template, so all this is correct:
$this->view->fullName = $localDetails['print_full_first_name']; // for printing only, not for editing
$this->view->firstName = $localDetails['edit_first_name']; // for edit in input field
$this->view->additionalComments => $customerDetails['edit_additional_comments'], // for edit in textarea field
$this->view->startDate = $localDetails['start_date']; // a know format, no escaping needed
$this->view->startTime = $localDetails['print_start_time']; // for printing only, not for editing
$this->view->pickupLocationName = $objPickupLocation->getPrintTranslatedLocationName();
 
8. For class methods:
8.1. Prefix with 'getPrint' only those methods, which returns html-escaped content (except the '<br />' code). So this means, that 'drop-down option lists', 'admin lists' CANNOT (!) be prefixed with 'getPrint' and must use just a regular 'get' prefix, i.e. 'getAdminList()'. While for i.e. getPrintShortPickupDate() is ok to be prefixed with 'getPrint'.

9. For translations of text, debug, okay and error messages:
9.1. Debug messages are NEVER translatable. They are flexible, might be often changed, and never visible to regular customers,
unless all three - WordPress WP_DEBUG = TRUE, WordPress WP_DEBUG_DISPLAY = TRUE and exact NS model class has it's of $debugMode = 1.
9.2. All Okay messages and all error messages MUST be translated, as they are seen for customers.
9.3. All models and controllers customers/admins output text has to be translated.
9.4. All front-end templates has to be translated.
9.5. All admin templates should be translated, but that is not mandatory.

10. Always try to avoid as much as we can of having a pure language texts calls in the controllers,
i.e. try to avoid "$title = $this->lang->getPrint(..);". The pure text calls should happen in models and templates.
Having that in controller is a bad idea, as that complicates system flexibility.

11. Language file coding standards:
11.1. Languages codes can be used anywhere - in admin, and front-end, for regular and AJAX queries, for WordPress menu items, and plugin-specific pages content, for WordPress role names, WordPress posts or even WordPress Widgets, so we don't want to stick to specific context for that language code, to avoid multiple replications and code chaos. So instead of that we are grouping all language codes only by Model Elements and nothing else. Period.
11.2. Language file should rows must be grouped ONLY by the element in the alphabetical order. Each element can have up to 4 sections - 2 content sections (that element observer, the actual element) and 2 okay / error message sections (one for that element observer, and one for the actual element).
11.3. The element naming should NEVER be based on things like:
	 'ADMIN' / 'NON-ADMIN' section (no 'admin' prefixes or suffixes allowed)
	 'AJAX' / 'NON-AJAX' language rows (no 'ajax' prefixes or suffixes allowed)
	 'ALERT' / 'ERROR' grouping for HTML errors VS Javascript Alerts (no 'alert' prefixes or suffixes allowed - we MUST always suffix those errors with the 'ERROR' suffix, despite is that a JS alert error or HTML error)
	 Suffixes / Prefixes like '_ROLE_NAME', 'ADMIN_MENU_' or silimar are NOT ALLOWED
11.4. There CANNOT be any global okay / error messages sections. Any okay / error message should be only in that actual element okay / error messages section.
11.5. For most common words, that are NOT describing the single element, we can have global common language rows. Those rows SHOULD not start with any of elements prefix.
11.6. The words '_SELECT', '_SHORT' etc. goes AFTER the name, i.e. we must use 'NS_ITEM_PAGE_SELECT' and NOT the 'NS_ITEM_SELECT_PAGE', nor the 'NS_SELECT_ITEM_PAGE'. That helps us to have clear grouping and all related element language rows for same purpose action will always be next to each other.
11.7. DO NOT translate the language file commments (those that start with '//') - they are used for identification, and should never be translated.

MVC:
For Model (MVC)
1. Error messages always are set in models, not controllers. In controllers we just pull these messages, aggregate them, and send them to view. Try to avoid having okay/error messages set in model observers - in that place rather choose to put a message into controller directly.
2. For model's save() method via $params we should submit only the values for database table columns, and do a clean-up / sanitization in the method. We should not check in the method inside the existance of related other element id (that should be done in the controller), nor we should check access rights, i.e. isManager / canEdit - that also should be done in the controller, while the canEdit() method itself should be defined in the model. We also should not pass to the model's save() method the date, time and date-format values separately, if that is not saved in database table, and we should pass only the 'timestamp' value instead of the previous 3 columns.
2.1. canEdit() should exists only in those models, that allows partners to edit them or create new via admin. For transactions, as it is very complex access check, it should do explicit check for the ability to edit order or check for the current user having manager rights. Because this uses other model, this check has to be done in the controller.
2.2. We should not have methods like public function canEdit($paramPartnerId). That means this element does not have partner_id column, and the check should be done externally.
3. We should never check for blog_id or ext_code in the model itself, unless that is a must (i.e. for observer to list data for current blog and extension, or to attach related output in desired language by i.e. item_sku). The only unique identifier there is should be that database table PRIMARY_KEY (id). And it is recommended in all these cases to pass that data via param.
4. There should be no 'public function getTranslatedDropdownOptionsByPartnerId($paramPartnerId = -1, ...) methods in classes - partner id (or id's array) should always go as a first parameter in main drop-down method, i.e. public function getTranslatedDropdownOptions($paramPartnerId = -1, ...)

BCNF DATABASE STANDART NOTES:
1. Even if we can theoretically fit additional fiels of X table into separate table as rows, WE DON'T DO that, unless that is i.e. "attribute" which values can be defined and used multiple times and it is can have more than 20 fields of that type (i.e. attributes). So that's wy in customers or orders tables we have so many columns, but that allows us to keep the database much more easier to read and understand even for beginner developers.

ARCHITECTURAL DECISIONS:
1. in front-end, Font-Awesome should be always loaded by default from the plugin after install / demo import, as if we load it from the theme, after theme's update it will fail to keep up with FA version, and the images won't be loaded, and our goal is to give the best possible view from start that is easiest to start.

## **General notes of S.O.L.I.D. MVC coding standards for begginers**

Here are the basic S.O.L.I.D. MVC coding standards for begginers to follow  

### 1. HTML:

* **img Tags**  
img tags do not have a tag like \</img>, so the correct way to actually close the tag should be like this `<img src="image.jpg" />`, but not like this `<img src="image.jpg">`

* **empty Tags**  
Another common mistakes come from empty tags like `<br />`, these tags **should not be used like** `<br>`

### 2. CSS layout:

* **Spacing between the selector and the opening bracket**  

When writing CSS begginers usually do not leave a space after the selector when opening braces, what they do is:

```css
.class{
	/*some code*/
}
```

When it should be: 

```css
.class {
	/*some code*/
}
```

Notice the little space between the brackets and the selector


* **Closing the brackets**  
Another thing begginers like to do is close the brackets on the same line as a property, e.g.


```css
.class {
	margin: 0;}
```

The correct way would be:

```css
.class {
	margin: 0;
}
```


* **Spacing between a property and its value**  
A common begginers mistake is to not leave a space between a property and its value, for example `margin:0;`, when it should be `margin: 0;`

* **Spaces between selectors**  

Often a begginer developer will try to space out his code as much as possible for better readability, but they over do it. There should be no space seperating selectors, example:
```css
.class1 {
	margin: 0;
}
.class2 {
	padding: 0;
}
```

**wrong:**

```css
.class1 {
	margin: 0;
}

.class2 {
	padding: 0;
}
```

* **Multiple Selectors**  
When you have multiple selectors a good practice is to separate them on a new line:

```css
.slector1,
.selector2 {
	/*Some code*/
}
```

**NOT:**

```css
.slector1, .selector2 {
	/*Some code*/
}
```

* **Section separation**  

The only things that can be separated are different sections, e.g.

```css

/***********************************************************************************/
/******************************** SECTION 1 **********************************/
/***********************************************************************************/

.section1-class1 {
	/*code*/
}
.section1-class2 {
	/*code*/
}
.section1-class3 {
	/*code*/
}

/***********************************************************************************/
/******************************** SECTION 2 **********************************/
/***********************************************************************************/

.section2-class1 {
	/*code*/
}
.section2-class2 {
	/*code*/
}
.section2-class3 {
	/*code*/
}

/*media queries should look like this*/

@media all and (max-width: 1000px) {
	.class1 {
		/*code*/
	}
	.class2 {
		/*code*/
	}
	.class3 {
		/*code*/
	}
}
```

### 3. PHP spacing

* **Single line echoes** 

Single line echos should always be closed without spaces and use the short PHP opening brackets, e.g.

```php
// What to do
<?=esc_html($var);?>

// What not to do

<?php esc_html($var); ?>
``` 

* **Colon use in IF/ELSE/FOREACH/ENDIF/WHILE/ENDWHILE**  

After all of these statements after a colon there should be a space and full `<?php ?>` tags should be used:

```html
<?php if(something): ?>
	// some HTML
<?php elseif(somethingElse): ?>
	// some HTML
<?php else: ?>
	// some HTML
<?php endif; ?>
```

**BAD:**

```php
<?php if(something):?>
	// some HTML
<?php elseif(somethingElse):?>
	// some HTML
<?php else:?>
	// some HTML
<?php endif;?>
```
