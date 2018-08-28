---
swagger: "2.0"
x-collection-name: Swagger
x-complete: 1
info:
  title: Swagger Hub Registry
  description: the-registry-api-for-swaggerhub
  contact:
    name: SwaggerHub
    url: http://swaggerhub.com
    email: info@swaggerhub.com
  version: 1.0.45
host: api.swaggerhub.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apis/{owner}/{api}:
    post:
      summary: Saves the provided Swagger definition
      description: Saves the provided swagger definition.
      operationId: saveDefinition
      x-api-path-slug: apisownerapi-post
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: body
        name: definition
        description: the Swagger definition of this API
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: force
        description: force update
      - in: query
        name: isPrivate
        description: Defines whether the API has to be private
      - in: path
        name: owner
        description: API or Domaion owner identifier
      - in: query
        name: version
        description: api version
      responses:
        200:
          description: OK
      tags:
      - APIs
      - Owner
  /apis/{owner}/{api}/{version}/.draft:
    put:
      summary: Saves the provided draft for a Swagger definition
      description: Saves the provided draft for a swagger definition.
      operationId: saveDraft
      x-api-path-slug: apisownerapiversion-draft-put
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: body
        name: definition
        description: the Swagger definition of this API
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: API owner identifier
      - in: path
        name: version
        description: version identifier
      responses:
        200:
          description: OK
      tags:
      - APIs
      - Owner
      - Version
      - ""
      - Draft
---