# OpenAPI\Client\DefaultApi

All URIs are relative to http://localhost:9003/api/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**smsSend()**](DefaultApi.md#smsSend) | **POST** /sms/send | Send a text message request.


## `smsSend()`

```php
smsSend($sms_send_request): \OpenAPI\Client\Model\SmsSendResponse
```

Send a text message request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Auth-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Auth-Token', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sms_send_request = new \OpenAPI\Client\Model\SmsSendRequest(); // \OpenAPI\Client\Model\SmsSendRequest

try {
    $result = $apiInstance->smsSend($sms_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->smsSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sms_send_request** | [**\OpenAPI\Client\Model\SmsSendRequest**](../Model/SmsSendRequest.md)|  |

### Return type

[**\OpenAPI\Client\Model\SmsSendResponse**](../Model/SmsSendResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
