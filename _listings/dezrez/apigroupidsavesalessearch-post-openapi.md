---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Saves Search Criteria to a Group
  version: 1.0.0
  description: Saves search criteria to a group.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/agency/savemeetingplace:
    post:
      summary: Saves a new meeting place to that particular agency
      description: Saves a new meeting place to that particular agency.
      operationId: Agency_SaveMeetingPlaceBydataContract
      x-api-path-slug: apiagencysavemeetingplace-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Saves
      - New
      - Meeting
      - Place
      - To
      - That
      - Particular
      - Agency
  /api/documentgeneration/saveenvelopetemplate:
    post:
      summary: Saves or updates the envelope template for an agency
      description: Saves or updates the envelope template for an agency.
      operationId: DocumentGeneration_SaveEnvelopeTemplateByenvelopeTemplate
      x-api-path-slug: apidocumentgenerationsaveenvelopetemplate-post
      parameters:
      - in: body
        name: envelopeTemplate
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Saves
      - Updates
      - Envelope
      - Templatean
      - Agency
  /api/documentgeneration/saveenvelopetemplatepack:
    post:
      summary: Saves or updates envelope template correspondence for a an agency
      description: Saves or updates envelope template correspondence for a an agency.
      operationId: DocumentGeneration_SaveEnvelopeTemplatePackByenvelopeTemplatePack
      x-api-path-slug: apidocumentgenerationsaveenvelopetemplatepack-post
      parameters:
      - in: body
        name: envelopeTemplatePack
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Saves
      - Updates
      - Envelope
      - Template
      - Correspondencea
      - Agency
  /api/todo/general/savetodo:
    post:
      summary: "Saves or Updates a General ToDo \r\nThis is currently used to save
        quick reminders"
      description: "Saves or updates a general todo \r\nthis is currently used to
        save quick reminders."
      operationId: GeneralToDo_SaveToDoBytoDoSave
      x-api-path-slug: apitodogeneralsavetodo-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: toDoSave
        description: A wrapper for the todo save data and the various data contracts
          needed
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Saves
      - S
      - General
      - ToDo
      - This
      - Is
      - Currently
      - Used
      - To
      - Save
      - Quick
      - Reminders
  /api/group/{id}/savesalessearch:
    post:
      summary: Saves Search Criteria to a Group
      description: Saves search criteria to a group.
      operationId: Group_SaveSalesSearchByidBysearchDataContract
      x-api-path-slug: apigroupidsavesalessearch-post
      parameters:
      - in: path
        name: id
        description: The id of the group
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: searchDataContract
        description: The groups search criteria
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Saves
      - Search
      - Criteria
      - To
      - Group
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