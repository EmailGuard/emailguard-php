# emailguardSdk\EmailApi

Analyzes an email for syntax, normalization, typo suggestions, role/public/relay/disposable signals. Invalid TLDs can return suggested_email and suggested_domain while syntax_validation remains false.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1EmailsDetectGet()**](EmailApi.md#apiV1EmailsDetectGet) | **GET** /api/v1/emails/detect | Detect email characteristics |


## `apiV1EmailsDetectGet()`

```php
apiV1EmailsDetectGet($email): \emailguardSdk\Model\EmailDetectResponse
```

Detect email characteristics

Analyzes an email for syntax, normalization, typo suggestions, role/public/relay/disposable signals. Invalid TLDs can return suggested_email and suggested_domain while syntax_validation remains false.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new emailguardSdk\Api\EmailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$email = 'email_example'; // string | Email address to analyze

try {
    $result = $apiInstance->apiV1EmailsDetectGet($email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailApi->apiV1EmailsDetectGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email** | **string**| Email address to analyze | |

### Return type

[**\emailguardSdk\Model\EmailDetectResponse**](../Model/EmailDetectResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
