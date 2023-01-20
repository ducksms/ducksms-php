# Ducksms\CreditApi

All URIs are relative to *https://ducksms.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**creditBalance**](CreditApi.md#creditBalance) | **GET** /api/v1/credits/balance | Credit Balance
[**creditHistory**](CreditApi.md#creditHistory) | **GET** /api/v1/credits/history | Credit History



## creditBalance

> \Ducksms\Model\CreditBalance creditBalance()

Credit Balance

Get available credit balance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\CreditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->creditBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditApi->creditBalance: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Ducksms\Model\CreditBalance**](../Model/CreditBalance.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## creditHistory

> \Ducksms\Model\CreditHistory creditHistory($page, $filter_type, $filter_sms_smsid)

Credit History

Get all credit history

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new Ducksms\Api\CreditApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Page number
$filter_type = credit; // string | Filter by credit type
$filter_sms_smsid = 1009771270; // int | Filter by sms id

try {
    $result = $apiInstance->creditHistory($page, $filter_type, $filter_sms_smsid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreditApi->creditHistory: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Page number | [optional]
 **filter_type** | **string**| Filter by credit type | [optional]
 **filter_sms_smsid** | **int**| Filter by sms id | [optional]

### Return type

[**\Ducksms\Model\CreditHistory**](../Model/CreditHistory.md)

### Authorization

[BearerToken](../../README.md#BearerToken)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

