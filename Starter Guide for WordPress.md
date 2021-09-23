# DEVELOPER STARTER GUIDE FOR WORDPRESS:
-----------------------------------------
1. Debug mode variable is only used in Models
2. In controllers we only use WordPress WP_DEBUG and WP_DEBUG_DISPLAY, sometimes we use WP_DEBUG_LOG and no local class debug variables.
    1) We use `StaticValidator::inWP_Debug()`, which is based on `WP_DEBUG_DISPLAY` constant if you want to perform actions (i.e. echo debug printing on screen).
    2) We use `StaticValidator::wpDebugLog()`, which is based on `WP_DEBUG_LOG` constant if you want to log your debug to file.  
4. In GetDetails functions, always have elseif with null prefill
5. No issets in templates, because the variables or information needs to be given proccesed.


# PHPSTORM INSPECTIONS TO DISABLE FOR MOST EFFECTIVE CODING:
-----------------------------------------------------------

***Effective coding** - we must focus on real errors and issues, and not on over simplyfing, and not over optimizing the code, because then other developers will struggle editing the code.*

1. Uncheck: Settings -> Inspections -> PHP -> Unnecessary local variable 
