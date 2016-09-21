## How to Use

The following section explains how to use the BroScript library in a new project.


## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

#### Authentication and Initialization
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| userKey | User Key |
| scriptKey | Script Key |



API client can be initialized as following.

```php
// Configuration parameters and credentials
$userKey = "userKey"; // User Key
$scriptKey = "scriptKey"; // Script Key

$client = new BroScriptClient($userKey, $scriptKey);
```

# Class Reference
## <a name="list_of_controllers"></a>List of Controllers

* [APIController](#api_controller)

## <a name="api_controller"></a>![Class: ](http://apidocs.io/img/class.png ".APIController") APIController


#### Get singleton instance
The singleton instance of the ``` APIController ``` class can be accessed from the API Client.
```php
$client = $client->getClient();
```

### <a name="clean_history"></a>![Method: ](http://apidocs.io/img/method.png ".APIController.cleanHistory") cleanHistory

> TODO: Add a method description

```php
function cleanHistory($chatId = NULL)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| chatId |  ``` Optional ```  | chat id |



#### Example Usage:
```php
$chatId = 'chat_id';

$result = $client->cleanHistory($chatId);

```




### <a name="templates"></a>![Method: ](http://apidocs.io/img/method.png ".APIController.templates") templates

> Get array with templates

```php
function templates()
```

#### Example Usage:
```php

$result = $client->templates();

```




### <a name="answers"></a>![Method: ](http://apidocs.io/img/method.png ".APIController.answers") answers

> Get answer

```php
function answers(
        $chatId = NULL,
        $contact = NULL,
        $external = NULL,
        $stopIsNull = false,
        $repeatIsNull = false)
```

#### Parameters: 

| Parameter | Tags | Description |
|-----------|------|-------------|
| chatId |  ``` Optional ```  | Chat id |
| contact |  ``` Optional ```  ``` Collection ```  | Object with information about concat |
| external |  ``` Optional ```  ``` Collection ```  | Object with information about external |
| stopIsNull |  ``` Optional ```  ``` DefaultValue ```  | Stop is null |
| repeatIsNull |  ``` Optional ```  ``` DefaultValue ```  | Stop is null |



#### Example Usage:
```php
$chatId = 'chat_id';
$contact = array('contact');
$external = array('external');
$stopIsNull = false;
$repeatIsNull = false;

$result = $client->answers($chatId, $contact, $external, $stopIsNull, $repeatIsNull);

```




[Back to List of Controllers](#list_of_controllers)


