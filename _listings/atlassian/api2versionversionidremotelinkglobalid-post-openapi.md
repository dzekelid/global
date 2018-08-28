---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Create or update remote version link with global id
  description: Create a remote version link via POST using the provided global ID.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /settings/theme/selected:
    get:
      summary: Get global theme
      description: |-
        Returns the globally assigned theme.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
      operationId: com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getGlobalTheme_get
      x-api-path-slug: settingsthemeselected-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Theme
  /api/2/attachment/meta:
    get:
      summary: Get global attachment settings
      description: "Returns the global attachment settings, that is, whether attachments
        are enabled and the maximum attachment size allowed.  \n  \nNote that there
        are also [project permissions](https://confluence.atlassian.com/x/yodKLg)
        that restrict whether users can create and delete attachments or not.  \n
        \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        None."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachmentMeta_get
      x-api-path-slug: api2attachmentmeta-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Attachment
      - Settings
  /api/2/configuration:
    get:
      summary: Get global settings
      description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
        in Jira. These settings determine whether optional features (for example,
        sub-tasks, time tracking, and others) are enabled. If time tracking is enabled,
        this method also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.ConfigurationResource.getConfiguration_get
      x-api-path-slug: api2configuration-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Settings
  /api/2/issue/{issueIdOrKey}/remotelink:
    delete:
      summary: Delete remote issue link by global id
      description: Deletes the issue's remote link with the given global ID.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.deleteRemoteIssueLinkByGlobalId_delete
      x-api-path-slug: api2issueissueidorkeyremotelink-delete
      parameters:
      - in: query
        name: globalId
        description: Global ID of a remote issue link to delete
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to delete a remote issue link for
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Link
      - By
      - Global
      - Id
  /api/2/version/{versionId}/remotelink/{globalId}:
    post:
      summary: Create or update remote version link with global id
      description: Create a remote version link via POST using the provided global
        ID.
      operationId: com.atlassian.jira.rest.v2.issue.VersionResource.createOrUpdateRemoteVersionLinkWithGlobalId_post
      x-api-path-slug: api2versionversionidremotelinkglobalid-post
      parameters:
      - in: path
        name: globalId
      - in: path
        name: versionId
      responses:
        200:
          description: OK
      tags:
      - Update
      - Remote
      - Version
      - Link
      - Global
      - Id
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---