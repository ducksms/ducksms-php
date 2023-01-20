# Ducksms\SmsApi

All URIs are relative to *https://ducksms.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**smsSend**](SmsApi.md#smsSend) | **POST** /api/v1/sms/send | Send Sms



## smsSend

> \Ducksms\Model\PreviewSmsSend smsSend($sms_schema)

Send Sms

Create a new sms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_schema = new \Ducksms\Model\SmsSchema(); // \Ducksms\Model\SmsSchema | Create a new sms

try {
    $result = $apiInstance->smsSend($sms_schema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->smsSend: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_schema** | [**\Ducksms\Model\SmsSchema**](../Model/SmsSchema.md)| Create a new sms | [optional]

### Return type

[**\Ducksms\Model\PreviewSmsSend**](../Model/PreviewSmsSend.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

