---
title: Regal.io Source
source-type: event
id: 1QTd6JKw53
redirect_from:  '/connections/sources/catalog/cloud-apps/regal-voice'
---
{% include content/source-region-unsupported.md %}

[Regal.io](https://regalvoice.com/?utm_source=segmentio&utm_medium=docs&utm_campaign=partners) is a next-gen customer engagement platform built for B2C services brands to proactively reach out to customers on voice and sms before they buy elsewhere.

This source is maintained by Regal.io. For any issues with the source, [contact the Regal.io Support team](mailto:support@regal.io).

> success ""
> **Good to know**: This page is about the Regal.io Segment source, which sends data _into_ Segment. There's also a page about the [Regal.io Segment destination](/docs/connections/destinations/catalog/regal-voice/), which receives data from Segment!

## Getting Started

1. From your workspace's [Sources catalog page](https://app.segment.com/goto-my-workspace/sources/catalog) click **Add Source**.
2. Search for "Regal.io" in the Sources Catalog, select click Regal.io, and click **Add Source**.
3. On the next screen, give the Source a nickname and configure any other settings.

   The nickname is used as a label in the Segment app, and Segment creates a related schema name in your warehouse.  The nickname can be anything, but we recommend using something that reflects the source itself and distinguishes amongst your environments (eg. SourceName_Prod, SourceName_Staging, SourceName_Dev).
5. Click **Add Source** to save your settings.
6. Copy the Write key from the Segment UI and email it to support@regal.io.

## Events

The table below lists events that Regal.io sends to Segment. These events appear as tables in your warehouse and as regular events in other Destinations. Regal.io includes the `userId` if available.

| Event name                   | Property description                                                                                  |
| ---------------------------- | ----------------------------------------------------------------------------------------------------- |
| agent.activity.updated       | An agent's activity status was changed.                                                               |
| call.completed               | An inbound or outbound call with a contact was completed. This includes calls that were not answered. |
| call.recording.available     | A call recording link is available.                                                                   |                           
| contact.subscribed           | A contact was subscribed to a marketing channel.                                                      |
| contact.unsubscribed         | A contact was unsubscribed from a marketing channel.                                                  |
| contact.attribute.edited     | A contact's attributes were edited by an agent.                                                       |
| contact.experiment.assigned  | A contact was assigned to an experiment.                                                              |
| scheduled.callback.requested | A callback was scheduled.                                                                             |
| sms.conversation.completed   | An SMS conversation between a contact and an agent was completed in the Regal.io agent desktop.    |
| sms.queued                   | An SMS was queued to be sent from Regal.io to contact.                                             |
| sms.sent                     | An SMS was sent from Regal.io to contact.                                                          |
| sms.undelivered              | An SMS was undelivered from Regal.io to contact.                                                   |
| sms.received                 | An SMS was received from a contact.                                                                   |
| task.canceled                | A call or SMS task was canceled.                                                                      |
| task.created                 | A call or SMS task was created.                                                                       |
| task.reservation.created     | A reservation was created for a task.                                                                 |
| task.reservation.accepted    | A reservation was accepted by an agent.                                                               |

## Event Properties

| Property Name                     | Description                                                                                                                                                                                                                                                                                                               |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `agent_activity_name`             | Name of agent's new availability status                                                                                                                                                                                                                                                                                   |
| `agent_availability`              | Availability of agent's previous activity status; can be true or false                                                                                                                                                                                                                                                    |
| `agent_email`                     | Email of the agent who took an action                                                                                                                                                                                                                                                                                     |
| `agent_previous_activity_name`    | Name of agent's previous availability status                                                                                                                                                                                                                                                                              |
| `agent_previous_availability`     | Availability of agent's previous activity status; can be true or false                                                                                                                                                                                                                                                    |
| `agent_time_in_previous_activity` | Time (in seconds) agent spent in previous activity status                                                                                                                                                                                                                                                                 |
| `call_id`                         | Task Id for the call                                                                                                                                                                                                                                                                                                      |
| `callback_timestamp`              | When the callback is scheduled for                                                                                                                                                                                                                                                                                        |
| `campaign_id`                     | Campaign Id                                                                                                                                                                                                                                                                                                               |
| `campaign_friendly_id`            | Campaign Friendly Id as seen in the app                                                                                                                                                                                                                                                                                   |
| `campaign_name`                   | Campaign name                                                                                                                                                                                                                                                                                                             |
| `cancelation_reason`              | Reason the task was canceled_by                                                                                                                                                                                                                                                                                           |
| `cancelation_source`              | Source of where the task was canceled                                                                                                                                                                                                                                                                                     |
| `canceled_by`                     | Includes the email of the user who canceled the task, if applicable                                                                                                                                                                                                                                                       |
| `changes`                         | Changes made for the contact.attribute_edited event                                                                                                                                                                                                                                                                       |
| `channel`                         | The marketing channel: "voice" or "SMS"                                                                                                                                                                                                                                                                                   |
| `completed_at`                    | UTC Timestamp when the task was completed_at                                                                                                                                                                                                                                                                              |
| `contact_phone`                   | Phone number of the contact_phone                                                                                                                                                                                                                                                                                         |
| `content`                         | Content of the message                                                                                                                                                                                                                                                                                                    |
| `direction`                       | INBOUND or OUTBOUND                                                                                                                                                                                                                                                                                                       |
| `disposition`                     | Task disposition                                                                                                                                                                                                                                                                                                          |
| `email`                           | The last email associated with the contact                                                                                                                                                                                                                                                                                |
| `ended_at`                        | UTC Timestamp when the conversation was ended                                                                                                                                                                                                                                                                             |
| `experiment_id`                   | Experiment ID                                                                                                                                                                                                                                                                                                             |
| `experiment_name`                 | Name of experiment                                                                                                                                                                                                                                                                                                        |
| `experiment_variant`              | Variant a contact was assigned to in an experiment                                                                                                                                                                                                                                                                        |
| `from_number`                     | Phone number that sent the message                                                                                                                                                                                                                                                                                        |
| `handle_time`                     | Full duration task was being handled, including talk time and wrap time (completed_at - started_at)                                                                                                                                                                                                                       |
| `ip`                              | The IP address from where the subscription update was initiated                                                                                                                                                                                                                                                           |
| `media_url`                       | Media URL (if it was an MMS)                                                                                                                                                                                                                                                                                              |
| `notes`                           | Task notes                                                                                                                                                                                                                                                                                                                |
| `objections`                      | Task objections                                                                                                                                                                                                                                                                                                           |
| `phone`                           | The phone number the subscription updated was applied to; phone number is the unique identifier for a contact in Regal.io                                                                                                                                                                                              |
| `queue`                           | Task Queue                                                                                                                                                                                                                                                                                                                |
| `recording_link` | Call recording link |
| `regal_voice_phone`               | Regal.io phone number                                                                                                                                                                                                                                                                                                  |
| `regal_voice_phone_internal_name` | Internal name of phone line displayed to agents
| `reserved_agent_email` | Email of the agent the task reservation is for
| `reserved_agent_full_name` | Full name of the agent the task reservation is for 
| `scheduling_agent_email`          | Email of the agent who scheduled the callback                                                                                                                                                                                                                                                                             |
| `scheduling_agent_fullname`       | Full name of the agent who scheduled the callback                                                                                                                                                                                                                                                                         |
| `scheduling_agent_id`             | Email of the agent who scheduled the callback                                                                                                                                                                                                                                                                             |
| `sms_conversation_id`             | Task ID for the conversation (if the SMS was part of a two-way conversation with an agent, rather than just an automated outbound sms)                                                                                                                                                                                    |
| `source`                          | Source of the subscription update. A source value that starts with "Brand." indicates that the subscription update was initiated by the Brand (outside of the Regal.io platform). A source value that starts with "RegalVoice." indicates that the subscription update was initiated through the Regal.io platform. |
| `started_at`                      | UTC timestamp when the conversation was started                                                                                                                                                                                                                                                                           |
| `talk_time`                       | Duration of conversation (ended_at - started_at)                                                                                                                                                                                                                                                                          |
| `target_agent_fullname`           | Full name of the agent who contact (and all contact's tasks) are assigned to                                                                                                                                                                                                                                              |
| `target_agent_id`                 | Email of the agent who contact (and all contact's tasks) are assigned to                                                                                                                                                                                                                                                  |
| `task_id`                         | Unique identifier for the task. Will match the `call_id` or `sms_conversation_id` of a completed task event.                                                                                                                                                                                                              |
| `text`                            | The exact text the contact was presented for opt in                                                                                                                                                                                                                                                                       |
| `timestamp`                       | Unix timestamp for when the event took place                                                                                                                                                                                                                                                                              |
| `to_number`                       | Phone number to which the message was spent                                                                                                                                                                                                                                                                               |
| `type`                            | Task Type                                                                                                                                                                                                                                                                                                                 |
| `wrapup_time`                     | Duration task was in wrap up (`completed_at` - `ended_at`)      

## Adding Destinations

Now that your Source is set up, you can connect it with Destinations.

Log into your downstream tools and check to see that your events appear as expected, and that they contain all of the properties you expect. If your events and properties don't appear, check the [Event Delivery](https://segment.com/docs/connections/event-delivery/) tool, and refer to the Destination docs for each tool for troubleshooting.

If there are any issues with how the events are arriving to Segment, [contact the Regal.io support team](mailto:support@regal.io).