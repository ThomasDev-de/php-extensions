# php-extensions
## Constants
### FILTER_VALIDATE_PHONE
This constant allowed only letters for a valid phone number.
```php
const FILTER_VALIDATE_PHONE = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[+]*[(]{0,1}[0-9]{1,4}[)]{0,1}[-\s\./0-9]*$~")
];
```
### FILTER_VALIDATE_SEX
This constant allowed only letters for gender recognition.
- `F`: female
- `M`: male
- `D`: divers
```php
const FILTER_VALIDATE_SEX = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(F|M|D){1}$~")
];
```
### FILTER_VALIDATE_STATUS
This constant allows to assign only letters for a status
- `Y`: yes
- `N`: no
```php
const FILTER_VALIDATE_STATUS = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(Y|N){1}$~")
];
```
### FILTER_VALIDATE_GUID
This constant only lets through GUID's
- `4f74d85c-2f9f-4d5a-9bb8-29ed234457a0`
```php
const FILTER_VALIDATE_GUID = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[0-9a-fA-F]{8}(-[0-9a-fA-F]{4}){3}-[0-9a-fA-F]{12}$~")
];
```
### FILTER_VALIDATE_URL_WITH_UMLAUTS
This constant allows URLs with umlauts.  
_Attention, umlauts are generally not permitted in URLs, but they can still occur._
```php
const FILTER_VALIDATE_URL_WITH_UMLAUTS = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^(http|ftp|https):\/\/[\w\-_]+(\.[\w\-_]+)+([\w\-\.,@?^=%&amp;:\/~\+#äöüÄÖÜ]*[\w\-\@?^=%&amp;\/~\+#])?$~")
];
```
### FILTER_VALIDATE_ARRAY_INT
This constant only allows arrays with integer values
- [1,12,2,4,"19"]
```php
const FILTER_VALIDATE_ARRAY_INT = [
    'filter' => FILTER_VALIDATE_INT,
    'flags' => FILTER_REQUIRE_ARRAY,
];
```
### FILTER_VALIDATE_ARRAY_STRING
This constant only allows arrays with string values
```php
const FILTER_VALIDATE_ARRAY_STRING = [
    'filter' => FILTER_DEFAULT,
    'flags' => FILTER_REQUIRE_ARRAY,
];
```
### FILTER_VALIDATE_DATE
This constant checks the value for correct formatting of a date.  
**It does not check for correctness!**
```php
const FILTER_VALIDATE_DATE = [
    'filter' => FILTER_VALIDATE_REGEXP,
    'options' => array('regexp' => "~^[0-9]{4}-(0[1-9]|1[0-2])-(0[1-9]|[1-2][0-9]|3[0-1])$~")
];
```