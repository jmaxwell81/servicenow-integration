# servicenow-integration
ServiceNow Configurable REST integration application

This repository consists of an XML Update Set containing the complete codebase for a scoped ServiceNow REST Integration application.

The application allows easy setup of a REST API endpoint, conditions under which the initial message will be sent ot the endpoint, and mapping from the source record to populate the REST message. The mapping can be a direct field map, including dot-walked fields to reference values, or a scripted mapping (this is also how you specify a fixed value). The field mapping also supports value mapping from source to target values for choice lists.

There is no need to set up a new business rule or UI action to send the REST message. The message is queued to send asynchronously any time a record is inserted or updated. By default, the application watches any task-based table, the Knowledge Base tables, and CMDB-based tables. It is also possible to send a single record to multiple endpoints; there is a separate table that tracks the foreign ID for the record against the REST endpoint.
