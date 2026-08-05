# emailguardSdk\RulesApi

Returns routing rules that map event types to one or more delivery channels. Each rule includes its enabled state and channel targets.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamNotificationsRulesGet()**](RulesApi.md#apiV1TeamNotificationsRulesGet) | **GET** /api/v1/team/notifications/rules | List notification rules |
| [**apiV1TeamNotificationsRulesPost()**](RulesApi.md#apiV1TeamNotificationsRulesPost) | **POST** /api/v1/team/notifications/rules | Create notification rule |
| [**apiV1TeamNotificationsRulesRuleIdDelete()**](RulesApi.md#apiV1TeamNotificationsRulesRuleIdDelete) | **DELETE** /api/v1/team/notifications/rules/{ruleId} | Delete notification rule |
| [**apiV1TeamNotificationsRulesRuleIdPut()**](RulesApi.md#apiV1TeamNotificationsRulesRuleIdPut) | **PUT** /api/v1/team/notifications/rules/{ruleId} | Update notification rule |


## `apiV1TeamNotificationsRulesGet()`

```php
apiV1TeamNotificationsRulesGet(): \emailguardSdk\Model\GetNotificationRulesResponse
```

List notification rules

Returns routing rules that map event types to one or more delivery channels. Each rule includes its enabled state and channel targets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamNotificationsRulesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->apiV1TeamNotificationsRulesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\GetNotificationRulesResponse**](../Model/GetNotificationRulesResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsRulesPost()`

```php
apiV1TeamNotificationsRulesPost($create_notification_rule_input): \emailguardSdk\Model\IdDataResponse
```

Create notification rule

Creates a rule that delivers matching events to the specified channels. At least one event type and one channel target are required.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_notification_rule_input = new \emailguardSdk\Model\CreateNotificationRuleInput(); // \emailguardSdk\Model\CreateNotificationRuleInput | Rule name, event types, and channel targets

try {
    $result = $apiInstance->apiV1TeamNotificationsRulesPost($create_notification_rule_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->apiV1TeamNotificationsRulesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_notification_rule_input** | [**\emailguardSdk\Model\CreateNotificationRuleInput**](../Model/CreateNotificationRuleInput.md)| Rule name, event types, and channel targets | |

### Return type

[**\emailguardSdk\Model\IdDataResponse**](../Model/IdDataResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamNotificationsRulesRuleIdDelete()`

```php
apiV1TeamNotificationsRulesRuleIdDelete($rule_id): \emailguardSdk\Model\MessageResponse
```

Delete notification rule

Permanently deletes a routing rule and its channel assignments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string | UUID of the notification rule to delete

try {
    $result = $apiInstance->apiV1TeamNotificationsRulesRuleIdDelete($rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->apiV1TeamNotificationsRulesRuleIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**| UUID of the notification rule to delete | |

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

## `apiV1TeamNotificationsRulesRuleIdPut()`

```php
apiV1TeamNotificationsRulesRuleIdPut($rule_id, $update_notification_rule_input): \emailguardSdk\Model\MessageResponse
```

Update notification rule

Updates a rule's name, description, event types, enabled flag, or channel targets. When `channels` is sent it replaces all existing targets.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\RulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string | UUID of the notification rule to update
$update_notification_rule_input = new \emailguardSdk\Model\UpdateNotificationRuleInput(); // \emailguardSdk\Model\UpdateNotificationRuleInput | Fields to update on the rule

try {
    $result = $apiInstance->apiV1TeamNotificationsRulesRuleIdPut($rule_id, $update_notification_rule_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RulesApi->apiV1TeamNotificationsRulesRuleIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**| UUID of the notification rule to update | |
| **update_notification_rule_input** | [**\emailguardSdk\Model\UpdateNotificationRuleInput**](../Model/UpdateNotificationRuleInput.md)| Fields to update on the rule | |

### Return type

[**\emailguardSdk\Model\MessageResponse**](../Model/MessageResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
