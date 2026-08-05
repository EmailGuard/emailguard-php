# emailguardSdk\MembersApi

Returns every member of the team, including role, profile fields, and join timestamp. Use the &#x60;user_id&#x60; field when calling member update or remove routes.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamMembersGet()**](MembersApi.md#apiV1TeamMembersGet) | **GET** /api/v1/team/members | List team members |
| [**apiV1TeamMembersUserIdDelete()**](MembersApi.md#apiV1TeamMembersUserIdDelete) | **DELETE** /api/v1/team/members/{userId} | Remove a team member |
| [**apiV1TeamMembersUserIdPatch()**](MembersApi.md#apiV1TeamMembersUserIdPatch) | **PATCH** /api/v1/team/members/{userId} | Update a team member role |


## `apiV1TeamMembersGet()`

```php
apiV1TeamMembersGet(): \emailguardSdk\Model\ListPublicTeamMembersResponse
```

List team members

Returns every member of the team, including role, profile fields, and join timestamp. Use the `user_id` field when calling member update or remove routes.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\MembersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamMembersGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MembersApi->apiV1TeamMembersGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\ListPublicTeamMembersResponse**](../Model/ListPublicTeamMembersResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamMembersUserIdDelete()`

```php
apiV1TeamMembersUserIdDelete($user_id): \emailguardSdk\Model\MessageResponse
```

Remove a team member

Removes a user from the team. Identify the member by user account UUID in the path. The team owner cannot be removed through this endpoint.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\MembersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User account UUID of the member to remove

try {
    $result = $apiInstance->apiV1TeamMembersUserIdDelete($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MembersApi->apiV1TeamMembersUserIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User account UUID of the member to remove | |

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

## `apiV1TeamMembersUserIdPatch()`

```php
apiV1TeamMembersUserIdPatch($user_id, $update_team_member_input): \emailguardSdk\Model\MessageResponse
```

Update a team member role

Changes a member's role or internal notes. Identify the member by user account UUID in the path (not the team membership record ID).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\MembersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_id = 'user_id_example'; // string | User account UUID of the member to update
$update_team_member_input = new \emailguardSdk\Model\UpdateTeamMemberInput(); // \emailguardSdk\Model\UpdateTeamMemberInput | New role and/or notes for the member

try {
    $result = $apiInstance->apiV1TeamMembersUserIdPatch($user_id, $update_team_member_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MembersApi->apiV1TeamMembersUserIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_id** | **string**| User account UUID of the member to update | |
| **update_team_member_input** | [**\emailguardSdk\Model\UpdateTeamMemberInput**](../Model/UpdateTeamMemberInput.md)| New role and/or notes for the member | |

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
