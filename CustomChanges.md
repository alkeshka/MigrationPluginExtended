# Custom Changes Made

## CustomerConverter.php
    
    - Added code to handle empty last and first name for customer 
        [ Lines 102 - 109 & 381 - 387 ]
    - Added code to handle empty zipcode, city and street
        [ Lines 389 - 398 ]
    - Added code to handle empty Salutations and set the not_specified as default 
        [ Lines 264 - 268 & 420 - 424 ]
    - Added new parameter to the constructor [ SalutationLookup, SystemConfigService, CustomerGroupRepository ]
        [ Line 84 ]
    - Added a new function for handling the customer group missing issue
        [ Lines 814 - 831 ]
    - Added if condition to Prefill missing customer group from config before required fields check
        [ Lines 119 - 122 ]
    - Updated function to set default group id
        [ Lines 232 - 243 ]

## shopware.xml

    - Added 'SalutationLookup' in the CustomerConverter argument
        [ Line 165 ]
    - Added 'SystemConfig', 'Tax.repository' and 'product_manufacturer.repository' in the ProductConverter argument
        [ Lines 119 - 121 ]
    - Added 'SalutationLookup' in the OrderConverter argument
        [ Line 179 ]

## config.xml

    - Created a new config field for the default tax
    - Created a new config field for default Manufacture

## ProductConverter

    - Added the constructor parameters
        [ SystemConfigService & EntityRepository (Tax Repository) ]
    - Added tax id fall back
        [ Lines 153 - 161 ]
    - Added a new function for getting the default tax details using the tax repository
        [ Lines 217 - 232 ]
    - Added a new for getting the default manufacture details using product_manufacture repository
        [ Lines 565 - 585 ]
    - Added the manufacture id fallback
        [ Lines 404 - 414 ]
    - Added the created at date fallback
        [ Lines 488 - 492 ]

## NumberRangeConverter.php

    - For the following error 
        [info] SWAG_MIGRATION__SHOPWARE_UNSUPPORTED_NUMBER_RANGE_TYPE
        Unsupported number range type
        NumberRange-Entity with source id "926" could not be converted because of unsupported type: sSERVICE1.
    - Please add the TYPE_MAPPING as needed for your project

## OrderConverter.php

    - Added 1970-01-01 00:00:00 as default date when there is no valid dateTime
        [ Lines 238 - 241 ]
    - Added the code to handle empty last and first name, zipcode, city and street
        [ Lines 518 - 534 ]
    - Added the constructor parameter for Salutation Lookup
    - Updated the if condition to skip the countryStateId 0
        [ Lines 686 - 695 ]

## ShopwareConverter.php

    - Replaced the validDate function to handle the invalid date situation
        [ Lines 113 - 141 ]

## NewsletterRecipientConverter.php
    
    - Added default value for _locale and shopId
        [ Lines 60 - 68 ]
        Set the _local to English and shopId to 1 Please change according