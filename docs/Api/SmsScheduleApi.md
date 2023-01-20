# Ducksms\SmsScheduleApi

All URIs are relative to *https://ducksms.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancelSmsSchedule**](SmsScheduleApi.md#cancelSmsSchedule) | **DELETE** /api/v1/sms/scheduled/{id} | Cancel Sms Schedule
[**listSmsSchedule**](SmsScheduleApi.md#listSmsSchedule) | **GET** /api/v1/sms/scheduled | List Sms Schedule



## cancelSmsSchedule

> \Ducksms\Model\CancelSmsSchedule cancelSmsSchedule($id)

Cancel Sms Schedule

Cancel existing sms schedule

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SmsScheduleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | 

try {
    $result = $apiInstance->cancelSmsSchedule($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsScheduleApi->cancelSmsSchedule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Ducksms\Model\CancelSmsSchedule**](../Model/CancelSmsSchedule.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## listSmsSchedule

> \Ducksms\Model\ListSmsSchedule listSmsSchedule($page, $filter_sender_name, $filter_type, $filter_message_type, $filter_status)

List Sms Schedule

List all the sms schedule

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SmsScheduleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Page number
$filter_sender_name = DUCKSMS; // string | Filter by sender id name
$filter_type = quick; // string | Filter by sms type
$filter_message_type = ascii; // string | Filter by sms message type
$filter_status = pending; // string | Filter by sms status

try {
    $result = $apiInstance->listSmsSchedule($page, $filter_sender_name, $filter_type, $filter_message_type, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsScheduleApi->listSmsSchedule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Page number | [optional]
 **filter_sender_name** | **string**| Filter by sender id name | [optional]
 **filter_type** | **string**| Filter by sms type | [optional]
 **filter_message_type** | **string**| Filter by sms message type | [optional]
 **filter_status** | **string**| Filter by sms status | [optional]

### Return type

[**\Ducksms\Model\ListSmsSchedule**](../Model/ListSmsSchedule.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

