---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/globalsearch/suggest:
    get:
      summary: Auto complete global search
      description: Auto complete global search.
      operationId: GlobalSearch_SuggestBytextBysuggestSize
      x-api-path-slug: apiglobalsearchsuggest-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: suggestSize
      - in: query
        name: text
        description: Text to search on
      responses:
        200:
          description: OK
      tags:
      - Auto
      - Complete
      - Global
      - Search
  /api/GlobalSearch:
    get:
      summary: The main endpoint for a global search across all entities in the system.
      description: The main endpoint for a global search across all entities in the
        system..
      operationId: GlobalSearch_IndexBytermByexcludeDeletedByexcludeArchivedBylastUpdated
      x-api-path-slug: apiglobalsearch-get
      parameters:
      - in: query
        name: excludeArchived
      - in: query
        name: excludeDeleted
      - in: query
        name: lastUpdated
        description: Get results from the last updated date
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: term
        description: Search term
      responses:
        200:
          description: OK
      tags:
      - The
      - Main
      - Endpointa
      - Global
      - Search
      - Across
      - ""
      - Entities
      - In
      - System
  /api/progression/lettings/resetdefaultmilestones:
    post:
      summary: Reset agency default milestones back to global defaults
      description: Reset agency default milestones back to global defaults.
      operationId: LettingsProgression_ResetMilestonesToDefault
      x-api-path-slug: apiprogressionlettingsresetdefaultmilestones-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Agency
      - Default
      - Milestones
      - Back
      - To
      - Global
      - Defaults
---