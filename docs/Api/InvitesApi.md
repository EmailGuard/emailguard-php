# emailguardSdk\InvitesApi

Returns invites that have not yet been accepted or expired. Each invite includes the target email, assigned role, and expiry time.

All URIs are relative to http://api.emailguard.co, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV1TeamMembersInvitesGet()**](InvitesApi.md#apiV1TeamMembersInvitesGet) | **GET** /api/v1/team/members/invites | List pending team invites |
| [**apiV1TeamMembersInvitesInviteIdDelete()**](InvitesApi.md#apiV1TeamMembersInvitesInviteIdDelete) | **DELETE** /api/v1/team/members/invites/{inviteId} | Cancel a pending invite |
| [**apiV1TeamMembersInvitesPost()**](InvitesApi.md#apiV1TeamMembersInvitesPost) | **POST** /api/v1/team/members/invites | Invite a team member |


## `apiV1TeamMembersInvitesGet()`

```php
apiV1TeamMembersInvitesGet(): \emailguardSdk\Model\ListPublicTeamInvitesResponse
```

List pending team invites

Returns invites that have not yet been accepted or expired. Each invite includes the target email, assigned role, and expiry time.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\InvitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->apiV1TeamMembersInvitesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitesApi->apiV1TeamMembersInvitesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\emailguardSdk\Model\ListPublicTeamInvitesResponse**](../Model/ListPublicTeamInvitesResponse.md)

### Authorization

[ApiKeyAuth](../../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV1TeamMembersInvitesInviteIdDelete()`

```php
apiV1TeamMembersInvitesInviteIdDelete($invite_id): \emailguardSdk\Model\MessageResponse
```

Cancel a pending invite

Revokes a pending invite so it can no longer be accepted. The invite is identified by its UUID from the list invites response.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\InvitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invite_id = 'invite_id_example'; // string | UUID of the pending invite to cancel

try {
    $result = $apiInstance->apiV1TeamMembersInvitesInviteIdDelete($invite_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitesApi->apiV1TeamMembersInvitesInviteIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invite_id** | **string**| UUID of the pending invite to cancel | |

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

## `apiV1TeamMembersInvitesPost()`

```php
apiV1TeamMembersInvitesPost($invite_team_member_input): \emailguardSdk\Model\MessageResponse
```

Invite a team member

Sends an email invite to join the team with the specified role. The invitee must accept before they appear in the members list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: ApiKeyAuth
$config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = emailguardSdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new emailguardSdk\Api\InvitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$invite_team_member_input = new \emailguardSdk\Model\InviteTeamMemberInput(); // \emailguardSdk\Model\InviteTeamMemberInput | Invitee email and role to assign on acceptance

try {
    $result = $apiInstance->apiV1TeamMembersInvitesPost($invite_team_member_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InvitesApi->apiV1TeamMembersInvitesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invite_team_member_input** | [**\emailguardSdk\Model\InviteTeamMemberInput**](../Model/InviteTeamMemberInput.md)| Invitee email and role to assign on acceptance | |

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
