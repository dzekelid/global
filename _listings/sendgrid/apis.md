---
name: SendGrid
x-slug: sendgrid
description: Delivering your transactional and marketing emails through the worlds
  largest cloud-based email delivery platform. Send with confidence.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/142-sendgrid.jpg
x-kinRank: "9"
x-alexaRank: "10000"
tags: Global
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/sendgrid/apis.md
specificationVersion: "0.14"
apis:
- name: SendGrid - Add Asm Suppressions Global
  x-api-slug: asmsuppressionsglobal-post
  description: |-
    **This endpoint allows you to add one or more email addresses to the global suppressions group.**

    A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/142-sendgrid.jpg
  humanURL: http://sendgrid.com
  baseURL: https://api.sendgrid.com//v3
  tags: API LIfeyclessss, Imports, Stack Network, Stack, Technology, SaaS, Emails,
    Emails, Messages, Messages, Relative Data, Service API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/sendgrid/asmsuppressionsglobal-post-openapi.md
- name: SendGrid - Delete Asm Suppressions Global Email
  x-api-slug: asmsuppressionsglobalemail-delete
  description: |-
    **This endpoint allows you to remove an email address from the global suppressions group.**

    A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/142-sendgrid.jpg
  humanURL: http://sendgrid.com
  baseURL: https://api.sendgrid.com//v3
  tags: API LIfeyclessss, Imports, Stack Network, Stack, Technology, SaaS, Emails,
    Emails, Messages, Messages, Relative Data, Service API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/sendgrid/asmsuppressionsglobalemail-delete-openapi.md
- name: SendGrid - Get Asm Suppressions Global Email
  x-api-slug: asmsuppressionsglobalemail-get
  description: |-
    **This endpoint allows you to retrieve a global suppression. You can also use this endpoint to confirm if an email address is already globally suppresed.**

    If the email address you include in the URL path parameter `{email}` is alreayd globally suppressed, the response will include that email address. If the address you enter for `{email}` is not globally suppressed, an empty JSON object `{}` will be returned.

    A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/142-sendgrid.jpg
  humanURL: http://sendgrid.com
  baseURL: https://api.sendgrid.com//v3
  tags: API LIfeyclessss, Imports, Stack Network, Stack, Technology, SaaS, Emails,
    Emails, Messages, Messages, Relative Data, Service API, Relative StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/global/master/_listings/sendgrid/asmsuppressionsglobalemail-get-openapi.md
x-common:
- type: x--net-library
  url: https://sendgrid.com/docs/Code_Examples/csharp.html
- type: x-api-gallery
  url: http://school.digger.api.gallery.streamdata.io
- type: x-api-stack
  url: http://sendgrid.stack.network
- type: x-base
  url: https://api.sendgrid.com
- type: x-blog
  url: http://blog.sendgrid.com/
- type: x-blog-rss
  url: http://feeds.feedburner.com/sendgrid/CDXr
- type: x-contact-form
  url: https://sendgrid.com/contact
- type: x-crunchbase
  url: http://www.crunchbase.com/company/sendgrid
- type: x-crunchbase
  url: https://crunchbase.com/organization/sendgrid
- type: x-developer
  url: https://sendgrid.com/developers
- type: x-documentation
  url: https://sendgrid.com/docs/index.html
- type: x-email
  url: privacy@sendgrid.com
- type: x-email
  url: legal@sendgrid.com
- type: x-email
  url: dpo@sendgrid.com
- type: x-forum
  url: http://support.sendgrid.com/forums
- type: x-github
  url: https://github.com/sendgrid
- type: x-go-library
  url: https://sendgrid.com/docs/Code_Examples/go.html
- type: x-ios-library
  url: https://sendgrid.com/docs/Code_Examples/ios.html
- type: x-java-library
  url: https://sendgrid.com/docs/Code_Examples/java.html
- type: x-labs
  url: http://labs.sendgrid.com/
- type: x-linkedin
  url: https://www.linkedin.com/company/sendgrid
- type: x-node-js-library
  url: https://sendgrid.com/docs/Code_Examples/nodejs.html
- type: x-partners
  url: https://sendgrid.com/partners
- type: x-perl-library
  url: https://sendgrid.com/docs/Code_Examples/perl.html
- type: x-php-library
  url: https://sendgrid.com/docs/Code_Examples/php.html
- type: x-pricing
  url: https://sendgrid.com/transactional-email/pricing
- type: x-privacy
  url: https://sendgrid.com/privacy
- type: x-python-library
  url: https://sendgrid.com/docs/Code_Examples/python.html
- type: x-ruby-library
  url: https://sendgrid.com/docs/Code_Examples/ruby.html
- type: x-security
  url: https://sendgrid.com/security
- type: x-selfservice-registration
  url: https://sendgrid.com/user/signup
- type: x-terms-of-service
  url: https://sendgrid.com/tos
- type: x-twitter
  url: https://twitter.com/SendGrid
- type: x-website
  url: http://sendgrid.com
- type: x-website
  url: https://sendgrid.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---