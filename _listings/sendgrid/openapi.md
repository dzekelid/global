swagger: "2.0"
x-collection-name: SendGrid
x-complete: 1
info:
  title: SendGrid
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /asm/suppressions/global:
    post:
      summary: Add Asm Suppressions Global
      description: |-
        **This endpoint allows you to add one or more email addresses to the global suppressions group.**

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.post
      x-api-path-slug: asmsuppressionsglobal-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
  /asm/suppressions/global/{email}:
    delete:
      summary: Delete Asm Suppressions Global Email
      description: |-
        **This endpoint allows you to remove an email address from the global suppressions group.**

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.email.delete
      x-api-path-slug: asmsuppressionsglobalemail-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
      - Email
    get:
      summary: Get Asm Suppressions Global Email
      description: |-
        **This endpoint allows you to retrieve a global suppression. You can also use this endpoint to confirm if an email address is already globally suppresed.**

        If the email address you include in the URL path parameter `{email}` is alreayd globally suppressed, the response will include that email address. If the address you enter for `{email}` is not globally suppressed, an empty JSON object `{}` will be returned.

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.email.get
      x-api-path-slug: asmsuppressionsglobalemail-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
      - Email