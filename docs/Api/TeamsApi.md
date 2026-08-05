# emailguardSdk\TeamsApi

Returns profile fields for the team associated with your API key.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamGet()**](TeamsApi.md#apiV1TeamGet) | **GET** /api/v1/team | Get team |
| [**apiV1TeamPatch()**](TeamsApi.md#apiV1TeamPatch) | **PATCH** /api/v1/team | Update team |


## `apiV1TeamGet()`

```php
apiV1TeamGet(): \emailguardSdk\Model\GetPublicTeamResponse
```

Get team

Returns profile fields for the team associated with your API key.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->apiV1TeamGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\GetPublicTeamResponse**](../Model/GetPublicTeamResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamPatch()`

```php
apiV1TeamPatch($update_team_input): \emailguardSdk\Model\GetPublicTeamResponse
```

Update team

Updates mutable team profile fields (name, emoji, URL, email). Send only the fields you want to change; omitted fields are left unchanged except `name`, which is required on every request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_team_input = new \emailguardSdk\Model\UpdateTeamInput(); // \emailguardSdk\Model\UpdateTeamInput | Team profile fields to update

try {
    $result = $apiInstance->apiV1TeamPatch($update_team_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->apiV1TeamPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_team_input** | [**\emailguardSdk\Model\UpdateTeamInput**](../Model/UpdateTeamInput.md)| Team profile fields to update | |

### Return type

[**\emailguardSdk\Model\GetPublicTeamResponse**](../Model/GetPublicTeamResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
