# emailguardSdk\BillingApi

Returns metered feature usage for the team&#39;s billing period. Defaults to the current period; use &#x60;range&#x3D;previous&#x60; or &#x60;range&#x3D;custom&#x60; with &#x60;start&#x60; and &#x60;end&#x60; to query other windows.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamBillingUsageGet()**](BillingApi.md#apiV1TeamBillingUsageGet) | **GET** /api/v1/team/billing/usage | Get billing usage |


## `apiV1TeamBillingUsageGet()`

```php
apiV1TeamBillingUsageGet($range, $start, $end): \emailguardSdk\Model\BillingUsageResponse
```

Get billing usage

Returns metered feature usage for the team's billing period. Defaults to the current period; use `range=previous` or `range=custom` with `start` and `end` to query other windows.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\BillingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$range = 'range_example'; // string | Period selector: current, previous, or custom
$start = 'start_example'; // string | Custom range start (RFC3339 or YYYY-MM-DD); required when range=custom
$end = 'end_example'; // string | Custom range end (RFC3339 or YYYY-MM-DD); required when range=custom

try {
    $result = $apiInstance->apiV1TeamBillingUsageGet($range, $start, $end);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingApi->apiV1TeamBillingUsageGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **range** | **string**| Period selector: current, previous, or custom | [optional] |
| **start** | **string**| Custom range start (RFC3339 or YYYY-MM-DD); required when range&#x3D;custom | [optional] |
| **end** | **string**| Custom range end (RFC3339 or YYYY-MM-DD); required when range&#x3D;custom | [optional] |

### Return type

[**\emailguardSdk\Model\BillingUsageResponse**](../Model/BillingUsageResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
