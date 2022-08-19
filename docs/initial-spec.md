# Introduction
## Purpose
The main purpose of the Smart Calendar Client API is to provide a simple interface for consuming community events, calendars, and contact information.
## Scope
* Provide a proxy for the Smart Calendar CalDAV and CardDAV Server.
* Detailed documentation for easy public usage.
* Allow consumers to search for events, calendars, and contacts. (will adopt JSON schema standards)
* Allow consumers to filter events, calendars and contacts. Non-exhaustive list is below.
  * Date/Time
  * Location
  * Name
  * Organizations

## Tech
* Python/Flask web API
* GCP Cloud Run
* [CalDAV Python client library](https://github.com/python-caldav/caldav) (consuming CalDAV server)
* CardDAV client interface is TBD
* Redis maybe implemented in the future if we begin to have scaling issues.

## Routes
NOTE - We will use something like swagger for the official API documentation.
* /events
  * query params
    * date_start
    * date_end
    * time_start
    * time_end
    * search
      * Name
* /calendars
  * query params
    * name
* /contacts
  * TBD