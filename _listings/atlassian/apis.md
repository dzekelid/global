---
name: Atlassian
x-slug: atlassian
description: Millions of users globally rely on Atlassian products every day for improving
  software development, project management, collaboration, and code quality.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
x-kinRank: "8"
x-alexaRank: "1656"
tags: Global
created: "2018-08-25"
modified: "2018-08-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/apis.md
specificationVersion: "0.14"
apis:
- name: The Confluence Cloud REST API - Get global theme
  x-api-slug: settingsthemeselected-get
  description: |-
    Returns the globally assigned theme.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/settingsthemeselected-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/settingsthemeselected-get-openapi.md
- name: Jira Cloud REST API - Get global attachment settings
  x-api-slug: api2attachmentmeta-get
  description: "Returns the global attachment settings, that is, whether attachments
    are enabled and the maximum attachment size allowed.  \n  \nNote that there are
    also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict
    whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2attachmentmeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2attachmentmeta-get-openapi.md
- name: Jira Cloud REST API - Get global settings
  x-api-slug: api2configuration-get
  description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
    in Jira. These settings determine whether optional features (for example, sub-tasks,
    time tracking, and others) are enabled. If time tracking is enabled, this method
    also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2configuration-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2configuration-get-openapi.md
- name: Jira Cloud REST API - Delete remote issue link by global id
  x-api-slug: api2issueissueidorkeyremotelink-delete
  description: Deletes the issue's remote link with the given global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2issueissueidorkeyremotelink-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2issueissueidorkeyremotelink-delete-openapi.md
- name: Jira Cloud REST API - Create or update remote version link with global id
  x-api-slug: api2versionversionidremotelinkglobalid-post
  description: Create a remote version link via POST using the provided global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2versionversionidremotelinkglobalid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2versionversionidremotelinkglobalid-post-openapi.md
- name: Jira Cloud REST API - Get my permissions
  x-api-slug: api2mypermissions-get
  description: |-
    Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

    If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

    If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

    If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

    The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

    Global permissions work in the same way regardless of the scope.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2mypermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2mypermissions-get-openapi.md
- name: Jira Cloud REST API - Get all permissions
  x-api-slug: api2permissions-get
  description: Returns all permissions that are present in the Jira instance - Global,
    Project and the global ones added by plugins
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2permissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/atlassian/api2permissions-get-openapi.md
x-common:
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/confluence/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/software/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/service-desk/swagger.v3.json
- type: x-website
  url: http://atlassian.com/
- type: x-website
  url: http://www.atlassian.com
- type: x-api-gallery
  url: http://att.dev.program.api.gallery.streamdata.io
- type: x-api-stack
  url: http://atlassian.stack.network
- type: x-blog
  url: http://blogs.atlassian.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/atlassian
- type: x-crunchbase
  url: http://www.crunchbase.com/company/atlassian
- type: x-email
  url: copyright@atlassian.com
- type: x-email
  url: trademarks@atlassian.com
- type: x-email
  url: sales@atlassian.com
- type: x-email
  url: ar_enterprise@atlassian.com
- type: x-email
  url: privacy@atlassian.com
- type: x-email
  url: eudatarep@atlassian.com
- type: x-email
  url: experts@atlassian.com
- type: x-email
  url: remittance@atlassian.com
- type: x-email
  url: ap@atlassian.com
- type: x-email
  url: procurement@atlassian.com
- type: x-github
  url: https://github.com/atlassian
- type: x-privacy-policy
  url: https://www.atlassian.com/legal/privacy-policy?_ga=2.188884514.868776184.1519225620-845241124.1519225620
- type: x-twitter
  url: https://twitter.com/atlassian
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---