# CreateNotificationRuleInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | [**\emailguardSdk\Model\NotificationRuleChannelInput[]**](NotificationRuleChannelInput.md) | One or more channel targets to notify when matching events occur. |
**conditions** | **array<string,mixed>** | Optional rule conditions (e.g. usage_threshold for USAGE_API_THRESHOLD). | [optional]
**description** | **string** | Optional longer description of what the rule does. | [optional]
**event_types** | **string[]** | Event type identifiers this rule listens for (at least one required). |
**is_enabled** | **bool** | When false, the rule is stored but does not deliver events. | [optional]
**name** | **string** | Display name for the rule. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
