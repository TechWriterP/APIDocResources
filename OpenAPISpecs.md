# Open API Specifications
- [OpenAPI](https://www.openapis.org/) is a specification for describing REST APIs.
- With OpenAPI, JSON objects, with a specific schema defines their naming, order, and contents.
- `paths`, `parameters`, `responses`, and `security` are some OpenAPI elements.

## OpenAPI elements
  ```
  paths:
  /pets:
    get:
      summary: List all pets
      operationId: listPets
      tags:
        - pets
      parameters:
        - name: limit
          in: query
          description: How many items to return at one time (max 100)
          required: false
          schema:
            type: integer
            format: int32
      responses:
        '200':
          description: An paged array of pets
          headers:
            x-next:
              description: A link to the next page of responses
              schema:
                type: string
          content:
            application/json:    
              schema:
                $ref: "#/components/schemas/Pets"
        default:
          description: unexpected error
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Error"
  ```
Here’s what these objects mean:
- `/pets` is the endpoint path.
- `get` is the HTTP method.
- `parameters` lists the parameters for the endpoint.
- `responses` lists the response from the request.
- `200` is the HTTP status code.
- `$ref` is a reference to another part of your implementation where the response is defined (in components). OpenAPI has a lot of $ref markers like this to keep your code clean and to facilitate re-use.
