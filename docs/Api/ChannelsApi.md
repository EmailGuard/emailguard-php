# emailguardSdk\ChannelsApi

Returns every delivery channel configured for the team (email, webhook, and other supported types). Use channel IDs when attaching targets to notification rules.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamNotificationsChannelsChannelIdDelete()**](ChannelsApi.md#apiV1TeamNotificationsChannelsChannelIdDelete) | **DELETE** /api/v1/team/notifications/channels/{channelId} | Delete notification channel |
| [**apiV1TeamNotificationsChannelsChannelIdPut()**](ChannelsApi.md#apiV1TeamNotificationsChannelsChannelIdPut) | **PUT** /api/v1/team/notifications/channels/{channelId} | Update notification channel |
| [**apiV1TeamNotificationsChannelsChannelIdTestPost()**](ChannelsApi.md#apiV1TeamNotificationsChannelsChannelIdTestPost) | **POST** /api/v1/team/notifications/channels/{channelId}/test | Test notification channel |
| [**apiV1TeamNotificationsChannelsGet()**](ChannelsApi.md#apiV1TeamNotificationsChannelsGet) | **GET** /api/v1/team/notifications/channels | List notification channels |
| [**apiV1TeamNotificationsChannelsPost()**](ChannelsApi.md#apiV1TeamNotificationsChannelsPost) | **POST** /api/v1/team/notifications/channels | Create notification channel |


## `apiV1TeamNotificationsChannelsChannelIdDelete()`

```php
apiV1TeamNotificationsChannelsChannelIdDelete($channel_id): \emailguardSdk\Model\MessageResponse
```

Delete notification channel

Permanently deletes a channel and removes it from any rules that reference it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string | UUID of the notification channel to delete

try {
    $result = $apiInstance->apiV1TeamNotificationsChannelsChannelIdDelete($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->apiV1TeamNotificationsChannelsChannelIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**| UUID of the notification channel to delete | |

### Return type

[**\emailguardSdk\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsChannelsChannelIdPut()`

```php
apiV1TeamNotificationsChannelsChannelIdPut($channel_id, $update_notification_channel_input): \emailguardSdk\Model\GetNotificationChannelResponse
```

Update notification channel

Updates a channel's display name or configuration. Send only fields you want to change.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string | UUID of the notification channel to update
$update_notification_channel_input = new \emailguardSdk\Model\UpdateNotificationChannelInput(); // \emailguardSdk\Model\UpdateNotificationChannelInput | Updated channel name and/or configuration

try {
    $result = $apiInstance->apiV1TeamNotificationsChannelsChannelIdPut($channel_id, $update_notification_channel_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->apiV1TeamNotificationsChannelsChannelIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**| UUID of the notification channel to update | |
| **update_notification_channel_input** | [**\emailguardSdk\Model\UpdateNotificationChannelInput**](../Model/UpdateNotificationChannelInput.md)| Updated channel name and/or configuration | |

### Return type

[**\emailguardSdk\Model\GetNotificationChannelResponse**](../Model/GetNotificationChannelResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsChannelsChannelIdTestPost()`

```php
apiV1TeamNotificationsChannelsChannelIdTestPost($channel_id): \emailguardSdk\Model\MessageResponse
```

Test notification channel

Sends a sample payload to a webhook channel to confirm the endpoint is reachable. On success the channel is marked verified.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string | UUID of the webhook channel to test

try {
    $result = $apiInstance->apiV1TeamNotificationsChannelsChannelIdTestPost($channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->apiV1TeamNotificationsChannelsChannelIdTestPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**| UUID of the webhook channel to test | |

### Return type

[**\emailguardSdk\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsChannelsGet()`

```php
apiV1TeamNotificationsChannelsGet(): \emailguardSdk\Model\GetNotificationChannelsResponse
```

List notification channels

Returns every delivery channel configured for the team (email, webhook, and other supported types). Use channel IDs when attaching targets to notification rules.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamNotificationsChannelsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->apiV1TeamNotificationsChannelsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\GetNotificationChannelsResponse**](../Model/GetNotificationChannelsResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsChannelsPost()`

```php
apiV1TeamNotificationsChannelsPost($create_notification_channel_input): \emailguardSdk\Model\GetNotificationChannelResponse
```

Create notification channel

Creates a delivery channel for the team. Email channels require verification; webhook channels can be verified with the test endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\ChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_notification_channel_input = new \emailguardSdk\Model\CreateNotificationChannelInput(); // \emailguardSdk\Model\CreateNotificationChannelInput | Channel name, type, and type-specific configuration

try {
    $result = $apiInstance->apiV1TeamNotificationsChannelsPost($create_notification_channel_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsApi->apiV1TeamNotificationsChannelsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_notification_channel_input** | [**\emailguardSdk\Model\CreateNotificationChannelInput**](../Model/CreateNotificationChannelInput.md)| Channel name, type, and type-specific configuration | |

### Return type

[**\emailguardSdk\Model\GetNotificationChannelResponse**](../Model/GetNotificationChannelResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
