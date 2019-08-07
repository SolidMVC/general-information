# S.O.L.I.D. MVC Micro-Framework
General Information

**SolidMVC** - a GDPR-compliant micro-framework that based on collection of most popular coding-standards (PSR-2, PSR-4 Autoloaders, Semantic Versioning, Unicode CLDR support, BCNF Database Structure) and Technologies (Font-Awesome) to allow any Object-Oriented Software Architect from C# or Java, PHP Software Architects comming to WordPress from Symfony or Laravel, to pick-up and start coding in WordPress withing the same day, without any need to learn any new coding standards. I, as software architect, developed the SolidMVC together with professors and lectors from worlds TOP-500 universities, that are the creators of Software Engineering Master Degree courses of Software Architecture and Design courses. The SolidMVC was developed in 4 years (2015-2019) and is licensed under almost unlimited - MIT-license, meaning that it can be used for both - commercial and non-commercial use. The example MVP (Minimum Viable Product) of SolidMVC is at w.org as "[https://wordpress.org/plugins/expandable-faq/ Expandable FAQ]". 

## **CODING STANDARDS ("Compliant With: <..>, <..>, <..>")**

Coding Standards list can be a similar to **tag cloud** in StackOverflow - here defined tags can be added automatically, but the new tags has to be approved by moderator:

[https://www.php-fig.org/psr/psr-2/ PSR-2] - created by PHP evangelists, but is pretty much cross-platform, any C# or JAVA developer can pick-up this.

[https://www.php-fig.org/psr/psr-4/ PSR-4 Autoloaders] - created by PHP evangelists, but is also, pretty much cross-platform, as in C# or JAVA the loading is done automatically as well.

[https://semver.org/spec/v2.0.0.html Semantic Versioning] - again, evolved from PHP.net's `version_compare()`, and became a cross-platform **dependency-hell** preventer.

[https://en.wikipedia.org/wiki/Boyce%E2%80%93Codd_normal_form BCNF Database Structure] - there can also be a lower level definition of [https://en.wikipedia.org/wiki/Third_normal_form Third Normal Form] or more strict - [https://en.wikipedia.org/wiki/Fourth_normal_form Fourth Normal Form]

[http://cldr.unicode.org/index Unicode CLDR KEY=>VALUE language package support] - Open-Source “Unicode CLDR” is cross-platform KEY=>VALUE translation-based solution for databases of GEO-CODING ([http://cldr.unicode.org/translation/country-names country names], city names, ares, Airport Codes (IATA), phone regions etc.), and is largely sponsored by Google.
_Notes: Google also developed Google AMP for WordPress (Accelerated mobile pages) and was main sponsor of WordCamp Europe 2018. As well as this is most popular language translation solution. Also it is the fastest solution, as the language data gets to the memory right away without parsing, can be edited by any editor, including Notepad++, and is suitable for enterprise project with different extensions on same code-base, where LANG_ITEM_TEXT in template, based on extension and loaded file might describe a car or a boat._

**POT (Portable Objects Template) files** - popular only within WordPress and WPML. The biggest drawback of it, that is is pretty-much commercial tool - the only useful editor is [https://poeditor.com/pricing/ PO-Editor], which is free to translate, but is paid for plugin developers to generate those .PO/.MO files. It is not cross-platform, it's file has to be parsed (is not native to the language) and is not suitable for extensions and large enterprise projects that needs to run different extensions on same code base.

----

## **MICRO-FRAMEWORK: <..>**

2 of 3 modern medium+ size plugins and themes runs on some kind of micro-framework, developed by the company or MIT-open-sourced.

**None** - for the WordPress plugins, that are not based on some kind of micro-framework.

**SolidMVC** - a GDPR-compliant micro-framework that based on collection of most popular coding-standards (PSR-2, PSR-4 Autoloaders, Semantic Versioning, Unicode CLDR support, BCNF Database Structure) and Technologies (Font-Awesome) to allow any Object-Oriented Software Architect from C# or Java, PHP Software Architects comming to WordPress from Symfony or Laravel, to pick-up and start coding in WordPress withing the same day, without any need to learn any new coding standards. I, as software architect, developed the SolidMVC together with professors and lectors from worlds TOP-500 universities, that are the creators of Software Engineering Master Degree courses of Software Architecture and Design courses. The SolidMVC was developed in 4 years (2015-2019) and is licensed under almost unlimited - MIT-license, meaning that it can be used for both - commercial and non-commercial use. The example MVP (Minimum Viable Product) of SolidMVC is at w.org as "[https://wordpress.org/plugins/expandable-faq/ Expandable FAQ]". 

[https://reduxframework.com/ Redux Framework] - popular solution for options for theme authors.

[http://unyson.io/ Unison framework] - also popular framework by theme authors, it was also used by older versions of Avada.

So keeping in mind, that I put 4 years to develop a micro-framework to create plugins, as well as there is many other micro-frameworks, as well used by hundreds of authors, as a micro-framework author, I'd really love to know who are enjoying and creating the plugins on given technology. As well as that could be a perfect way to understand whose coding quality is high enough and to develop the websites by using the "same-family" code-base, which may prevent the mentioned "**dependecy hell**" as well as "**updateness**".

----

## **USE-CASES:**

two example situations, when it would be super valuable:

1. “I’m building a widget for DirectAdmin that will patch the plugins automatically, but not update them”. For this I need to avoid thing, called “dependecy hell”, and this is solved only if the plugin follows the “Semantic Versioning” (SemVer) coding standard.

2. I just hired a new developer in my company, who is software architect coming from C#. So he is familiar with PSR-2 and PSR-4 Autoloaders (meaning, he don't have to bother understanding includes). His task is to take some similar plugin from w.org, and make a "Dietary product list" plugin - so what he does, is he first searches at w.org for similar scope plugins (in this case "FAQ plugin") that is "PSR-2"-compliant, as this is the code he can pick-up and start editing at DAY 1.


----

## **A PROVE THAT WORDPRESS USERS CARE ABOUT CODING STANDARDS:**

The evidences bellow are based facts and research, plus sale results on my own system for pasts 4 years:

1. **"KNOW YOUR CUSTOMER".** At WordCamp Europe 2018 one of the main talks was "**WordPress in 2019**" by @noel_tock (Noel Tock), which was about where WordPress was 10 years ago and where it will be next year, and how it changed. Session - https://2018.europe.wordcamp.org/session/wordpress-in-2019/ , slides - https://www.slideshare.net/ntock/wordpress-in-2019 . From the attached images bellow, you see, that if in 2010 WordPress had a coverage from "representational "About.us" site" to the very complex website (enterprise solution), then in 2018 it is already different - the "About Us" websites are now fully covered by Facebook, for those who need a bit more modifications for the "About.us" websites - they use Wix.com. WordPress is used then, when either - privacy matters a lot, meaning everything has to be self-hosted, including internal analytics, no Google tracking, no policy given big company like Facebook - and Facebook does that a lot, it tries to set 'their favorable' political views, as well as even to use your friend as a 'product' by their newest "Include donation campaign to your birthday". So there is a lot of people who resist to that - but everyone who I met, who does resist to Facebook, does not install WhatsApp, Messenger or Facebook apps on their phones, and use Facebook only via Web - all they were **smart**, **tech-savvy** people. So they know what is PGP key, ProtonMail.ch, HTTPS and Signal App. Very often they also have at least basic understand about security, and this is where often pop-us questions about data validations and coding standards - they may not be a developers or so, but they have heard in one or another conference some term, what is secure and high-quality, and they want an "MVC website with S.O.L.I.D. and there has to be HTTPS and semantic versioning". Also they want "PHP7, and object-oriented code". That's what I hear often from those people. So despite they may not know exactly what it does, they got recommendations from their IT friends, on some Facebook IT group, to what to use for their product. So how to discover those WordPress plugins at w.org right now, whose code follows these security standards, and design principles - we can't, just via Google index we may pick-up some data from the content. White there has to be a way to do that.

![WordPress in 2010](https://i.imgur.com/Knsn6RO.jpg "WordPress in 2010")

![WordPress in 2018](https://i.imgur.com/3E2y1ky.jpg "WordPress in 2018")

''*NOTE: If someone has a question, what the empty white space in the middle represent there in a picture of 2018 - that is **SaaS** software - a niche websites, like Booking.com or AirBnb.com, that focuses on specific problem and provide **multi-tenancy** feature - allowing customers to create their own profile of seller and make money'' 

2. **WORDPRESS FOR ENTERPRISE** & **WORDPRESS FOR PUBLIC SERVICES**. Today WordPress is much more Enterprise-accepted than it was in 2010, so that blue bar for today should be moved even further. The big companies started to trust WordPress. In Summer, 2018, I convinced probably the first capital in European Union - Vilnius City Municipality, to ditch their current custom made website, and switch to WordPress. And they did that - so now WordPress is being used for **PUBLIC SERVICES**. And I go even further - last weekend I pitched the SolidMVC, as the in VoteCraft hackathon in European Parliament Bureau in Vilnius. I been working in Digital Democracy (Online Petitions and Internet Voting) field for past 5 years, did my scientific research, involved in to that Vilnius University proffers and even a Dean of Faculty of Mathematics and Informatics - that's how the SolidMVC has born - it is not just a micro-framework for C#'ers or JAVA'ers to start writing their code immediately without any need to learn additional coding standards, SolidMVC is also **secure-enough** to use if for **elections**, by starting local elders of city areas elections online with secret-voting. That includes cryptography, and even digital signatures - and WordPress already has plugins in E-Signature field like this one - https://www.secure.approveme.com/demo/ ). So things moving forward, and even government organizations started to trust WordPress security.

3. **EDUCATE THE WORLD**. 10 years ago nor Mayors of the Cities, nor Ministers at the Parliament had any idea about how the WordPress is different from Symfony, or PHP from JAVA. Today they have that knowledge. WordPress leads the **33% of the whole internet** - so that also put a lot of responsibility and ability to educate the world - educate them about **security**, **coding-standards**, **programming languages**, **frameworks**, **micro-frameworks**, **principles** and **techniques**. So the main question is here - do we want to make the world smarter, if so - then let we give our customers more details about micro-framework and coding standards used - not everybody will dig-down to it, but **people and curious** - that is given to use by the nature, they will Google or ask - their friend or in plugins support forum - what it is, and how to eat that. And the message will spread.

4. **CUSTOM-WORKS TO PLUGIN & STATS OF "TYPICAL WP PLUGIN BUYER" IN 2019**. By taking an example of mine Reservations plugin sold on Envato for ~2000 times, I can say, that:
 a. **Only 15 customers of those 2000 (less than 0,1%)** had no idea of what they are doing - meaning they tried to upload plugin as a theme, or whole package ZIP, not just the plugin's ZIP.
 b. **500 customers (20%)** were individual developers, doing the website for their customer - they really did cared about security, and scalability-ensuring patterns (like BCNF-database structure and MVC).
 c. **1500 customers (75%)**, where the **Web-Development Agencies** (with 3-10 employees, of whose 1-8 were developers), who are doing websites for their end-customers, which is often is medium to enterprise companies (100-1000 employees). 50% of those agencies did **custom-works** to the plugin. And they bought the plugin just because they known **how to do the custom works** with it, without learning anything new. Meaning they needed the **MVC**, **S.O.L.I.D.** and plugin support for **Unicode CLDR** (Key=>VALUE pairs) to add the Geo-Data in their language i.e. country names, city names, phone area names and so on, on what they are working. So they changed the plugin's behavior to fit their medium/enterprise business customer needs, i.e. a business rule, that if object is rented in state X, for a Y days, and it was returned before the noon, then do not charge additional day costs - the rules that you cannot predict by filters or hooks - or you would need 100,000 filters and hooks support and 1 million pages documentation for all them. That would not work for the larger business, as nobody would want to learn now to hook to and what is the filter names of each bigger plugin.

5. **WHEN FILTERS & HOOKS ARE GREAT**:
 a. I love the WordPress because of it's filters and hooks - the ability to hook to the WordPress core **from a plugin** - but at he same time keep in mind that WordPress has probably over 100 people who been writing it's documentation of hooks in last 15 years - the regular plugin authors does not have this luxurity, plus **nobody would want to learn the names of filters of the plugin that does not have at least 1 million active installations and 10 millions downloads**, especially if that is web-agency who bought that plugin for use in that 1 particular customer's website and they are **done** and goes to next project.
 b. Also it is great for child themes of some kind of theme.
 c. Also, for **cross-plugin** WordPress plugins - i.e. "ReCaptcha integration" plugin (if it is not done by the plugin), "SMTP mailing settings" plugins, "Google Analytics" plugin or "WPML" language plugin (while I personally think that WordPress Multisite with Network-Enabled plugin and linking by ID's is much better, more stable, and more scalable solution, plus it is free).
 d. All other bigger plugins, have no need to have filter or action hooks, if they don't want to (''a choice in favor'') - I does complicate the testing of that plugin if it has UnitTests, as you don't know if the function 5+3 will always return 8. So instead of filters-and-hooks these plugins use **extension-points** for i.e. **Captcha Provider** (i.e. ReCaptcha), **Notification method** (i.e. SMS Provider) or **Payment Method** (i.e. PayPal), where they add their payment method library's folder to **/wp-content/plugins/GreatSystem/Libraries/** folder, and then use a **transpiler class**, i.e.:
```php
<?php
final class PayPalToGreatSystemTranspiler implements GreatSystemPaymentMethodInterface
{
<..>
}
```
 e. And here the **GreatSystemPaymentMethodInterface** has all the required method and in documentation is clearly described what each method implementation does. So there is no need then to write a 10,000 pages documentation with 10,000 filter names, just make one class that is testable and suitable for TDD (Test-Driven-Development) and can be tested with PHPUnit on PHPStorm via "/wp-content/plugins/GreatPluginTests/" plugin, if that payment methods comes pre-installed or from '/wp-content/plugins/PayPalForGreatSystemTests/Init.php'.
 f. So with my, **enterprise-ready**, plugin I may hook to cross-plugin type plugin like WPML but not vice-versa. 

6. **WHEN THE POT (Portable Objects Template) IS GREAT**:
 a. It is cool that WordPress core made in POT. It is a platform, not a product for niche market, so there is no **WordPost**, **WordArticle** etc. - but if it would, the nobody would ever want to maintain different code-base for every extension - that is for what POT is absolutely not suitable.
 b. Also the POT files are **great for themes** - I believe that themes has to be light and fast and **should not** go into **plugin territory**.
 c. POT files might be also great for some small one/two file plugins, that does not need any micro-framework, like "EasySMTP". Also POT can be useful for 'hook-based' general-purpose plugin like WooCommerce. 
 d. But that is only one option. Besides the **WooCommmerce** there is other products, for other market needs. Especially for the companies, who don't like WooCommerce and it's ads-full interface and promotion of other WooCoomerce product / extensions in WooCommerce admin, as well as those who focus on fast and scalable solutions for medium-size to enterprise companies, and when they look a products that have a defined use-case scenario, i.e. **Hotel Booking**, without any need to configure thousands of options before launch.
 e. So for all those 'd' cases - it is **enough** that plugin just have a **text-domain** registration, would apply plugin locale filter before loading it's language file file (doesn't matter it is Unicode CLDR or POT) and register **'load_textdomain'** and **'load_plugin_textdomain'** - that is enough that the w.org would be able to fully process through GlotPress the plugin name and description for translation, which is important for multilingual w.org website - you can see that right here - the 5 lines are available for translation - https://translate.wordpress.org/projects/wp-plugins/expandable-faq/dev/lt/default . And the Source code of the mail controller is here - https://plugins.trac.wordpress.org/browser/expandable-faq/trunk/Controllers/MainController.php
 f. The excerpt with only the 'i18n' method of SolidMVC micro-framework, of MVP (extension-less boilerplate) is below:
```php
<?php
final class MainController
{
    // Because loading of language text is not allowed in the very early time, we use constants to simulate language text behavior, just the text is English
    const LANG_ERROR_CLONING_IS_FORBIDDEN_TEXT = 'Error in __clone() method: Cloning instances of the class in the Rental System is forbidden.';
    const LANG_ERROR_UNSERIALIZING_IS_FORBIDDEN_TEXT = 'Error in __wakeup() method: Unserializing instances of the class in the Rental System is forbidden.';
    const LANG_ERROR_SESSIONS_ARE_DISABLED_IN_SERVER_TEXT = 'Warning: Sessions are disabled in your server configuration. Please enabled sessions. As a slower &amp; less secure workaround you can use virtual session via cookies, but that is not recommended.';
    const LANG_ERROR_PLEASE_UPGRADE_PHP_TEXT = 'Sorry, %s requires PHP %s or higher. Your current PHP version is %s. Please upgrade your server Php version.';
    const LANG_ERROR_PLEASE_UPGRADE_WP_TEXT = 'Sorry, %s requires WordPress %s or higher. Your current WordPress version is %s. Please upgrade your WordPress setup.';
    const LANG_ERROR_EXTENSION_NOT_EXIST_PLUGIN_CHILD_THEME_TEXT = 'Sorry, but %s extension does not exist neither in %s plugin directory, nor in %s child theme folder, nor in it&#39;s parent %s theme&#39;s folder.';
    const LANG_ERROR_EXTENSION_NOT_EXIST_PLUGIN_THEME_TEXT = 'Sorry, but %s extension does not exist neither in %s plugin directory, nor in %s theme folder.';
    const LANG_ERROR_UNKNOWN_NAME_TEXT = 'Unknown name';
    const LANG_ERROR_DEPENDENCIES_ARE_NOT_LOADED_TEXT = 'Dependencies are not loaded';
    const LANG_ERROR_CONF_WITHOUT_ROUTING_IS_NULL_TEXT = '$confWithoutRouting is NULL';
    const LANG_ERROR_CONF_IS_NULL_TEXT = '$conf is NULL';
    const LANG_ERROR_LANG_IS_NULL_TEXT = '$lang is NULL';
    const LANG_ERROR_IN_METHOD_TEXT = 'Error in &#39;%s&#39; method: %s!';

    // Configuration object reference
    private $confWithoutRouting         = NULL;
    private $conf                       = NULL;
    private $lang                       = NULL;
    private $canProcess                 = FALSE; // Have to be in main controller, as we don't use that for abstract controller
    private static $dependenciesLoaded  = FALSE;

    // <..>

    /**
     * Internationalization.
     * Load the language file, only if it is not yet loaded
     *
     * @access private
     * @return null|\ExpandableFAQ\Models\Language\Language
     * @throws \Exception
     */
    private function i18n()
    {
        if(static::$dependenciesLoaded === FALSE)
        {
            throw new \Exception(static::LANG_ERROR_DEPENDENCIES_ARE_NOT_LOADED_TEXT);
        }

        // Singleton pattern - load the language file, only if it is not yet loaded
        if(is_null($this->lang) && static::$dependenciesLoaded === TRUE)
        {
            // Assign routing to conf, only if it is not yet assigned
            $conf = $this->conf();

            if(is_null($conf))
            {
                throw new \Exception(static::LANG_ERROR_CONF_IS_NULL_TEXT);
            }

            // Traditional WordPress plugin locale filter
            // Note 1: We don't want to include the rows bellow to language model class, as they are a part of controller
            // Note 2: Keep in mind that, if the translation do not exist, plugin will load a default english translation file
            $locale = apply_filters('plugin_locale', get_locale(), $this->confWithoutRouting->getTextDomain());

            // Load textdomain
            // Loads MO file into the list of domains.
            // Note 1: If the domain already exists, the inclusion will fail. If the MO file is not readable, the inclusion will fail.
            // Note 2: On success, the MO file will be placed in the $l10n global by $domain and will be an gettext_reader object.

            // See 1: http://geertdedeckere.be/article/loading-wordpress-language-files-the-right-way
            // See 2: https://ulrich.pogson.ch/load-theme-plugin-translations
            // wp-content/languages/<PLUGIN_FOLDER_NAME>/lt_LT.mo
            load_textdomain($this->confWithoutRouting->getTextDomain(), $this->confWithoutRouting->getGlobalLangPath().$locale.'.mo');
            // wp-content/plugins/ExpandableFAQ/Languages/<EXT_FOLDER_NAME>/lt_LT.mo
            load_plugin_textdomain($this->confWithoutRouting->getTextDomain(), FALSE, $this->confWithoutRouting->getLocalLangRelPath());

            $this->lang = new \ExpandableFAQ\Models\Language\Language(
                $this->confWithoutRouting->getTextDomain(), $this->confWithoutRouting->getGlobalLangPath(), $conf->getLocalLangPath(), $locale, FALSE
            );
        }

        return $this->lang;
    }
    // <..>
}
```
## **General notes of S.O.L.I.D. MVC coding standards for begginers**

Here are the basic S.O.L.I.D. MVC coding standards for begginers to follow  

### 1. HTML:

* **img Tags**  
img tags do not have a tag like \</img>, so the correct way to actually close the tag should be like this `<img src="image.jpg" />`, but not like this `<img src="image.jpg">`

* **empty Tags**  
Another common mistakes come from empty tags like `<br />`, these tags **should not be used like** `<br>`

### 2. CSS layout:

* **Spacing between the selector and the opening bracket**  

When writting CSS begginers usually do not leave a space after the selector when opening braces, what they do is:

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
Another thing beginers like to do is close the brackets on the same line as a property, e.g.


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
When you have multiple selectors a good practice is to seperate them on a new line:

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

* **Section seperation**  

The only things that can be seperated are differenct sections, e.g.

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

```php
<?php if(something): ?>
	<--! some HTML -->
<?php elseif(somethingElse): ?>
	<--! some HTML -->
<?php else: ?>
	<--! some HTML -->
<?php endif; ?>
```

**BAD:**

```php
<?php if(something):?>
	<--! some HTML -->
<?php elseif(somethingElse):?>
	<--! some HTML -->
<?php else:?>
	<--! some HTML -->
<?php endif;?>
```
