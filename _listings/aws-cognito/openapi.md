swagger: "2.0"
x-collection-name: AWS Cognito
x-complete: 1
info:
  title: AWS Cognito Merged API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AdminUserGlobalSignOut:
    get:
      summary: Admin User Global Sign Out
      description: Signs out users from all devices, as an administrator.
      operationId: adminUserGlobalSignOut
      x-api-path-slug: actionadminuserglobalsignout-get
      parameters:
      - in: query
        name: Username
        description: The user name
        type: string
      - in: query
        name: UserPoolId
        description: The user pool ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
      - Global Sign Out
  /?Action=GlobalSignOut:
    get:
      summary: Global Sign Out
      description: Signs out users from all devices.
      operationId: globalSignOut
      x-api-path-slug: actionglobalsignout-get
      parameters:
      - in: query
        name: AccessToken
        description: The access token
        type: string
      responses:
        200:
          description: OK
      tags:
      - Sign Out