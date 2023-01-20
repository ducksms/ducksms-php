# Ducksms\SenderIDApi

All URIs are relative to *https://ducksms.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createSender**](SenderIDApi.md#createSender) | **POST** /api/v1/senders | Create a Sender ID
[**deleteSender**](SenderIDApi.md#deleteSender) | **DELETE** /api/v1/senders/{id} | Delete a Sender ID
[**getSender**](SenderIDApi.md#getSender) | **GET** /api/v1/senders/{id} | Get a single Sender ID
[**listSender**](SenderIDApi.md#listSender) | **GET** /api/v1/senders | List Sender ID
[**updateSender**](SenderIDApi.md#updateSender) | **POST** /api/v1/senders/{id} | Update a Sender ID



## createSender

> \Ducksms\Model\CreatedSender createSender($sender)

Create a Sender ID

Create a new sender id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SenderIDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sender = new \Ducksms\Model\Sender(); // \Ducksms\Model\Sender | Create a new sender

try {
    $result = $apiInstance->createSender($sender);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderIDApi->createSender: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sender** | [**\Ducksms\Model\Sender**](../Model/Sender.md)| Create a new sender | [optional]

### Return type

[**\Ducksms\Model\CreatedSender**](../Model/CreatedSender.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## deleteSender

> \Ducksms\Model\DeletedSender deleteSender($id)

Delete a Sender ID

Delete an existing sender id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SenderIDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->deleteSender($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderIDApi->deleteSender: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Ducksms\Model\DeletedSender**](../Model/DeletedSender.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getSender

> \Ducksms\Model\GetSender getSender($id)

Get a single Sender ID

Get details on a single sender id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SenderIDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->getSender($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderIDApi->getSender: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Ducksms\Model\GetSender**](../Model/GetSender.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## listSender

> \Ducksms\Model\ListSender listSender($page, $filter_name, $filter_status)

List Sender ID

List all the senders

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SenderIDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Page number
$filter_name = DUCKSMS; // string | Filter by sender name
$filter_status = active; // string | Filter by sender status

try {
    $result = $apiInstance->listSender($page, $filter_name, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderIDApi->listSender: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Page number | [optional]
 **filter_name** | **string**| Filter by sender name | [optional]
 **filter_status** | **string**| Filter by sender status | [optional]

### Return type

[**\Ducksms\Model\ListSender**](../Model/ListSender.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## updateSender

> \Ducksms\Model\UpdatedSender updateSender($id, $sender)

Update a Sender ID

Update an existing sender id

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SenderIDApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 
$sender = new \Ducksms\Model\Sender(); // \Ducksms\Model\Sender | Update an existing sender id

try {
    $result = $apiInstance->updateSender($id, $sender);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SenderIDApi->updateSender: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **sender** | [**\Ducksms\Model\Sender**](../Model/Sender.md)| Update an existing sender id | [optional]

### Return type

[**\Ducksms\Model\UpdatedSender**](../Model/UpdatedSender.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

