---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get all permissions
  description: Returns all permissions that are present in the Jira instance - Global,
    Project and the global ones added by plugins
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
  /api/2/mypermissions:
    get:
      summary: Get my permissions
      description: |-
        Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

        If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

        If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

        If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

        The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

        Global permissions work in the same way regardless of the scope.
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getMyPermissions_get
      x-api-path-slug: api2mypermissions-get
      parameters:
      - in: query
        name: issueId
        description: Id of the issue to scope returned permissions for
      - in: query
        name: issueKey
        description: Key of the issue to scope returned permissions for
      - in: query
        name: permissions
        description: A comma separated list of permission keys to check
      - in: query
        name: projectId
        description: Id of project to scope returned permissions for
      - in: query
        name: projectKey
        description: Key of project to scope returned permissions for
      responses:
        200:
          description: OK
      tags:
      - My
      - Permissions
  /api/2/permissions:
    get:
      summary: Get all permissions
      description: Returns all permissions that are present in the Jira instance -
        Global, Project and the global ones added by plugins
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getAllPermissions_get
      x-api-path-slug: api2permissions-get
      responses:
        200:
          description: OK
      tags:
      - Permissions
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