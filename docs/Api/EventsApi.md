# emailguardSdk\EventsApi

Returns recent notification delivery events for polling integrations. Use this to inspect what was sent and when without configuring a webhook receiver.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamNotificationsEventsGet()**](EventsApi.md#apiV1TeamNotificationsEventsGet) | **GET** /api/v1/team/notifications/events | List notification events |


## `apiV1TeamNotificationsEventsGet()`

```php
apiV1TeamNotificationsEventsGet(): \emailguardSdk\Model\GetNotificationEventsResponse
```

List notification events

Returns recent notification delivery events for polling integrations. Use this to inspect what was sent and when without configuring a webhook receiver.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamNotificationsEventsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->apiV1TeamNotificationsEventsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\GetNotificationEventsResponse**](../Model/GetNotificationEventsResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
