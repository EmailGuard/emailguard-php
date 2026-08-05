# NotificationRuleResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | [**\emailguardSdk\Model\NotificationRuleChannelResponse[]**](NotificationRuleChannelResponse.md) | Channel targets notified when the rule matches. | [optional]
**conditions** | **array<string,mixed>** | Optional conditions (e.g. usage threshold percents). | [optional]
**created_at** | **string** | When the rule was created (RFC3339). | [optional]
**description** | **string** | Optional longer description. | [optional]
**event_types** | **string[]** | Event types that trigger this rule. | [optional]
**id** | **string** | Rule record ID. | [optional]
**is_enabled** | **bool** | Whether the rule is actively delivering events. | [optional]
**name** | **string** | Display name for the rule. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
