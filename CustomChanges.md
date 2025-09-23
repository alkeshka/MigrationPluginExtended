# Custom Changes Made

## CustomerConverter.php
    
    - Added code to handle empty last and first name for customer 
        [ Lines 102 - 109 && 381 - 387 ]
    - Added code to handle empty zipcode, city and street
        [ Lines 389 - 398 ]
    - Added code to handle empty Salutations and set the not_specified as default 
        [ Lines 264 - 268 && 420 - 424 ]
    - Added new parameter to the constructor [ SalutationLookup ]
        [ Line 84 ]

## shopware.xml

    - Added 'SalutationLookup' in the CustomerConverter argument
        [ Line 165 ]