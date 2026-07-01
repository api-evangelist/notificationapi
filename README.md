# NotificationAPI (notificationapi)

NotificationAPI is notifications infrastructure for developers. A single REST API and drop-in in-app inbox component send multi-channel notifications - email, SMS, mobile and web push, in-app inbox, automated voice call, and Slack - while managing user identities, per-user preferences and opt-outs, templates, scheduling, and delivery logs. All calls are scoped to a clientId and authenticated with HTTP Basic auth.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/notificationapi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/notificationapi/refs/heads/main/apis.yml)

## Tags

- Notifications
- Messaging
- Email
- SMS
- Push
- In-App Inbox

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### NotificationAPI Send API

Sends a notification to a user across the channels configured for the notification type - email, SMS, push, web push, in-app inbox, voice call, and Slack - with template parameters, per-channel overrides, and retract support via POST /sender and POST /sender/retract.

- **Human URL:** [https://docs.notificationapi.com/reference/send](https://docs.notificationapi.com/reference/send)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Send
- Notifications
- Multi-Channel

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/send)
- [API Reference](https://docs.notificationapi.com/reference/api-reference)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI Schedule API

Schedules notifications for future delivery by passing an ISO 8601 schedule value to the Send API, then updates or cancels them by trackingId via PATCH and DELETE /schedule/{trackingId}.

- **Human URL:** [https://docs.notificationapi.com/reference/schedule](https://docs.notificationapi.com/reference/schedule)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Schedule
- Notifications
- Delayed Delivery

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/schedule)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI Users Identify API

Creates or updates the users you notify with their contact identifiers - email, phone number, push and web-push tokens, timezone, and Slack channel - via POST /users/{userId}, authenticated with a per-user HMAC signature.

- **Human URL:** [https://docs.notificationapi.com/reference/identify-user](https://docs.notificationapi.com/reference/identify-user)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Users
- Identify
- Contacts

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/identify-user)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI User Preferences API

Sets and deletes per-user, per-notification, per-channel delivery preferences and opt-outs - off/instant/hourly/daily/weekly/monthly - via POST /user_preferences/{userId} and DELETE /users/{userId}/preferences.

- **Human URL:** [https://docs.notificationapi.com/reference/set-user-preferences](https://docs.notificationapi.com/reference/set-user-preferences)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Preferences
- Opt-Out
- Subscriptions

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/set-user-preferences)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI Notifications Config API

Configures notifications and their subNotifications - independently subscribable subcategories such as per-project or per-topic channels - via PUT and DELETE /notifications/{notificationId}/subNotifications/{subNotificationId}.

- **Human URL:** [https://docs.notificationapi.com/reference/create-sub-notification](https://docs.notificationapi.com/reference/create-sub-notification)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Notifications
- Configuration
- SubNotifications

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/create-sub-notification)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI In-App Inbox API

Powers the drop-in in-app inbox component - reads a user's INAPP_WEB notifications with pagination and marks them opened, clicked, archived, actioned, or replied via GET and PATCH /users/{userId}/notifications/INAPP_WEB.

- **Human URL:** [https://docs.notificationapi.com/reference/in-app-notifications](https://docs.notificationapi.com/reference/in-app-notifications)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- In-App Inbox
- Notifications
- Read State

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/in-app-notifications)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NotificationAPI Logs API

Queries delivery and event logs filtered by date range, notification, channel, user, status, and trackingId via POST /logs/query.

- **Human URL:** [https://docs.notificationapi.com/reference/query-logs](https://docs.notificationapi.com/reference/query-logs)
- **Base URL:** `https://api.notificationapi.com/{clientId}`

#### Tags

- Logs
- Analytics
- Delivery

#### Properties

- [Documentation](https://docs.notificationapi.com/reference/query-logs)
- [OpenAPI](openapi/notificationapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/notificationapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/notificationapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/notificationapi-com)
- [LinkedIn](https://www.linkedin.com/company/notificationapi)
- [Website](https://www.notificationapi.com/)
- [Documentation](https://docs.notificationapi.com)
- [Plans](plans/notificationapi-plans-pricing.yml)
- [Rate Limits](rate-limits/notificationapi-rate-limits.yml)
- [Fin Ops](finops/notificationapi-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
