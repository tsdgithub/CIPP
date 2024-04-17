---
description: View and amend notifications for your CIPP App
---

# Notifications

Configure notifications from CIPP.

CIPP provides alert notifications for Tenants and CIPP actions, sent as one combined table in an email or webhook body.

* [Tenant Alerts](https://github.com/KelvinTegelaar/CIPP/blob/website/docs/user/tenantadministration/alerts/README.md) create notifications regarding changes within a tenant. See that help page for more information on managing those alerts.
* CIPP Alerts relate to changes initiated via the CIPP platform.

### Available CIPP Alerts

* New Accounts created via CIPP
* Removed Accounts via CIPP
* New Applications added via CIPP
* New Policies added via CIPP
* New Standards added via CIPP
* Removed Standards via CIPP
* Token Refresh Events

### Sending Methods

#### E-mail

Enter a many email addresses as you need, separated by a comma.

Email will be sent from the service account used for the SAM Wizard. The account must have a (shared) mailbox available. If you do not have a mailbox available on the account the log will state we could not send out the notifications.

{% hint style="info" %}
Sent Items Notification emails **do not save** to the CIPP account's _Sent Items_ folder.
{% endhint %}

#### Webhook

Enter a webhook URL. Data is formatted based on the receiving server:

| Service              | Format                                                |
| -------------------- | ----------------------------------------------------- |
| _webhook.office.com_ | A basic HTML formatted table.                         |
| _slack.com_          | A separate markdown-formatted message for each alert. |
| _discord.com_        | A basic HTML formatted table.                         |
| All other services   | JSON array of data values.                            |



{% hint style="info" %}
Custom Webhook Formatting Need something different for your webhook? Can you write PowerShell? Submit a PR on this repo: [CIPP-API\Scheduler\_CIPPNotifications](https://github.com/KelvinTegelaar/CIPP-API/tree/dev/Scheduler\_CIPPNotifications).
{% endhint %}



### Feature Requests / Ideas

Please raise any [feature requests](https://github.com/KelvinTegelaar/CIPP/issues/new?assignees=\&labels=enhancement%2Cno-priority\&projects=\&template=feature.yml\&title=%5BFeature+Request%5D%3A+) on GitHub.