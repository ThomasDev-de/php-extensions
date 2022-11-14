# php-extensions

```php
/**
* This constant allowed only letters for a valid phone number.
*
* p.e. +49 115 12 12 116
*/
const FILTER_VALIDATE_PHONE = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[+]*[(]{0,1}[0-9]{1,4}[)]{0,1}[-\s\./0-9]*$~")
];

/**
* This constant allowed only letters for gender recognition
*
* <ul>
* <li>F: female</li>
* <li>M: male</li>
* <li>D: divers</li>
* </ul>
*/
public const FILTER_VALIDATE_SEX = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(F|M|D){1}$~")
];

/**
* <ul>
* <li>Y: yes</li>
* <li>N: no</li>
* </ul>
*/
public const FILTER_VALIDATE_STATUS = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(Y|N){1}$~")
];

/**
* <ul>
* <li>Y: yes</li>
* </ul>
*/
public const FILTER_VALIDATE_STATUS_Y = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(Y){1}$~")
];

/**
* @example 4f74d85c-2f9f-4d5a-9bb8-29ed234457a0
*/
public const FILTER_VALIDATE_GUID = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[0-9a-fA-F]{8}(-[0-9a-fA-F]{4}){3}-[0-9a-fA-F]{12}$~")
];

public const FILTER_VALIDATE_URL_WITH_UMLAUTS = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(http|ftp|https):\/\/[\w\-_]+(\.[\w\-_]+)+([\w\-\.,@?^=%&amp;:\/~\+#äöüÄÖÜ]*[\w\-\@?^=%&amp;\/~\+#])?$~")
];

/**
* @example [1,12,2,4,"19"]
*/
public const FILTER_VALIDATE_ARRAY_INT = [
    'filter' => FILTER_VALIDATE_INT,
    'flags' => FILTER_REQUIRE_ARRAY,
];

public const FILTER_VALIDATE_ARRAY_STRING = [
    'filter' => FILTER_DEFAULT,
    'flags' => FILTER_REQUIRE_ARRAY,
];

/**
* @example 1970-01-01
*/
public const FILTER_VALIDATE_DATE = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[0-9]{4}-(0[1-9]|1[0-2])-(0[1-9]|[1-2][0-9]|3[0-1])$~")
];
```