# Custom Changes Made

## CustomerConverter.php
    
    - Added code to handle empty last and first name for customer 
        [ Lines 102 - 109 & 381 - 387 ]
    - Added code to handle empty zipcode, city and street
        [ Lines 389 - 398 ]
    - Added code to handle empty Salutations and set the not_specified as default 
        [ Lines 264 - 268 & 420 - 424 ]
    - Added new parameter to the constructor [ SalutationLookup ]
        [ Line 84 ]

## shopware.xml

    - Added 'SalutationLookup' in the CustomerConverter argument
        [ Line 165 ]
    - Added 'SystemConfig' and 'Tax.repository' in the ProductConverter argument
        [ Lines 119 - 120 ]

## config.xml

    - Created a new config filed for the default tax field

## ProductConverter

    - Added the constructor parameters
        [ SystemConfigService & EntityRepository (Tax Repository) ]
    - Added tax id fall back
        [ Lines 153 - 161 ]
    - Added a new function for getting the default tax details using the tax repository
        [ Lines 217 - 232 ]
    
## NumberRangeConverter.php

    - For the following error 
        [info] SWAG_MIGRATION__SHOPWARE_UNSUPPORTED_NUMBER_RANGE_TYPE
        Unsupported number range type
        NumberRange-Entity with source id "926" could not be converted because of unsupported type: sSERVICE1.
    - Please add the TYPE_MAPPING as needed for your project

