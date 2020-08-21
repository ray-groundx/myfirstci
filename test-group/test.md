# ReDoc Interactive Demo

## Swagger Petstore \(1.0.0\)

Download OpenAPI specification:[Download](https://redocly.github.io/redoc/openapi.yaml)

This is a sample server Petstore server. You can find out more about Swagger at [http://swagger.io](http://swagger.io/) or on [irc.freenode.net, \#swagger](http://swagger.io/irc/). For this sample, you can use the api key `special-key` to test the authorization filters.

## Cross-Origin Resource Sharing

This API features Cross-Origin Resource Sharing \(CORS\) implemented in compliance with [W3C spec](https://www.w3.org/TR/cors/). And that allows cross-domain communication from the browser. All responses have a wildcard same-origin which makes them completely public and accessible to everyone, including any code on any site.

Petstore offers two forms of authentication:

* API Key
* OAuth2 OAuth2 - an open protocol to allow secure authorization in a simple and standard method from web, mobile and desktop applications.

### petstore\_auth

Get access to data while protecting your account credentials. OAuth2 is also a safer and more secure way to give you access.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Security Scheme Type</th>
      <th style="text-align:left">OAuth2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">implicit OAuth Flow</td>
      <td style="text-align:left">
        <p> <b>Authorization URL:</b> http://petstore.swagger.io/api/oauth/dialog</p>
        <p> <b>Scopes:</b>
        </p>
        <ul>
          <li>
            <p><code>write:pets</code> -</p>
            <p>modify pets in your account</p>
          </li>
          <li>
            <p><code>read:pets</code> -</p>
            <p>read your pets</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### api\_key

For this sample, you can use the api key `special-key` to test the authorization filters.

|  Security Scheme Type |  API Key |
| :--- | :--- |
|  Header parameter name: |  api\_key |

Everything about your Pets

### Add a new pet to the store

Add new pet to the store inventory.

**cookie Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>cookieParam</p>
        <p>required</p>
      </th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**header Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Accept-Language</th>
      <th style="text-align:left">
        <p>string</p>
        <p>Default: en-AU</p>
        <p>Example: en-US</p>
        <p>The language you prefer for messages. Supported values are en-AU, en-CA,
          en-GB, en-US</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**Request Body schema:application/jsonapplication/xml**

Pet object that needs to be added to the store

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">
        <p>object</p>
        <p>Categories this pet belongs to</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>name</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>The name given to a pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>photoUrls</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>Array of strings &lt;url&gt; &lt;= 20 items</p>
        <p>The list of URL to a cute photos featuring pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">friend</td>
      <td style="text-align:left">object Recursive</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Array of objects (Tag) non-empty</p>
        <p>Tags attached to the pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;available&quot; &quot;pending&quot; &quot;sold&quot;</p>
        <p>Pet status in the store</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">petType</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Type of a pet</p>
        <p>cat</p>
        <p>cat</p>
        <p>dog</p>
        <p>bee</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>huntingSkill</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>Default: &quot;lazy&quot;</p>
        <p>Enum: &quot;clueless&quot; &quot;lazy&quot; &quot;adventurous&quot; &quot;aggressive&quot;</p>
        <p>The measured skill for hunting</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet

Sandbox server

https://petstore.swagger.io/sandbox/pet

####  Request samples

* Payload
* C\#
* PHP

Content type

application/json

application/xml

`{`

* `"category":`

  `{`

  * `"name": "string",`
  * `"sub":`

    `{`

    * `"prop1": "string"`

    `}`

  `},`

* `"name": "Guru",`
* * `"friend": { },`
* * `"status": "available",`
* `"petType": "cat",`
* `"huntingSkill": "adventurous"`

`}`

### Update an existing pet

**cookie Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>cookieParam</p>
        <p>required</p>
      </th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**header Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Accept-Language</th>
      <th style="text-align:left">
        <p>string</p>
        <p>Default: en-AU</p>
        <p>Example: en-US</p>
        <p>The language you prefer for messages. Supported values are en-AU, en-CA,
          en-GB, en-US</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**Request Body schema:application/jsonapplication/xml**

Pet object that needs to be added to the store

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">
        <p>object</p>
        <p>Categories this pet belongs to</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>name</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>The name given to a pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>photoUrls</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>Array of strings &lt;url&gt; &lt;= 20 items</p>
        <p>The list of URL to a cute photos featuring pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">friend</td>
      <td style="text-align:left">object Recursive</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Array of objects (Tag) non-empty</p>
        <p>Tags attached to the pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;available&quot; &quot;pending&quot; &quot;sold&quot;</p>
        <p>Pet status in the store</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">petType</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Type of a pet</p>
        <p>cat</p>
        <p>cat</p>
        <p>dog</p>
        <p>bee</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>huntingSkill</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>Default: &quot;lazy&quot;</p>
        <p>Enum: &quot;clueless&quot; &quot;lazy&quot; &quot;adventurous&quot; &quot;aggressive&quot;</p>
        <p>The measured skill for hunting</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet

Sandbox server

https://petstore.swagger.io/sandbox/pet

####  Request samples

* Payload
* PHP

Content type

application/json

application/xml

`{`

* `"category":`

  `{`

  * `"name": "string",`
  * `"sub":`

    `{`

    * `"prop1": "string"`

    `}`

  `},`

* `"name": "Guru",`
* * `"friend": { },`
* * `"status": "available",`
* `"petType": "cat",`
* `"huntingSkill": "adventurous"`

`}`

### Find pet by ID

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>petId</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>integer &lt;int64&gt;</p>
        <p>Deprecated</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet/{petId}

Sandbox server

https://petstore.swagger.io/sandbox/pet/{petId}

####  Response samples

* 200

Content type

application/json

application/xml

`{`

* `"id": 0,`
* `"category":`

  `{`

  * `"id": 0,`
  * `"name": "string",`
  * `"sub":`

    `{`

    * `"prop1": "string"`

    `}`

  `},`

* `"name": "Guru",`
* * `"friend": { },`
* `"tags":`

  `[`

  * `{`

    * `"id": 0,`
    * `"name": "string"`

    `}`

  `],`

* `"status": "available",`
* `"petType": "cat",`
* `"huntingSkill": "adventurous"`

`}`

### Updates a pet in the store with form data

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>petId</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>integer &lt;int64&gt;</p>
        <p>ID of pet that needs to be updated</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**Request Body schema: application/x-www-form-urlencoded**

<table>
  <thead>
    <tr>
      <th style="text-align:left">name</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Updated status of the pet</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet/{petId}

Sandbox server

https://petstore.swagger.io/sandbox/pet/{petId}

### Deletes a pet

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>petId</p>
        <p>required</p>
      </th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**header Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">api_key</th>
      <th style="text-align:left">
        <p>string</p>
        <p>Example: Bearer &lt;TOKEN&gt;</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet/{petId}

Sandbox server

https://petstore.swagger.io/sandbox/pet/{petId}

### uploads an image

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>petId</p>
        <p>required</p>
      </th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**Request Body schema: application/octet-stream**

Default server

https://petstore.swagger.io/v2/pet/{petId}/uploadImage

Sandbox server

https://petstore.swagger.io/sandbox/pet/{petId}/uploadImage

####  Response samples

* 200

Content type

application/json

`{`

* `"code": 0,`
* `"type": "string",`
* `"message": "string"`

`}`

### Finds Pets by status

Multiple status values can be provided with comma separated strings

**query Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>status</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>Array of strings [ 1 .. 3 ] items</p>
        <p>Items Enum: &quot;available&quot; &quot;pending&quot; &quot;sold&quot;</p>
        <p>Status values that need to be considered for filter</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/pet/findByStatus

Sandbox server

https://petstore.swagger.io/sandbox/pet/findByStatus

####  Response samples

* 200

Content type

application/json

application/xml

`[`

* `{`

  * `"id": 0,`
  * `"category":`

    `{`

    * `"id": 0,`
    * `"name": "string",`
    * `"sub":`

      `{`

      * `"prop1": "string"`

      `}`

    `},`

  * `"name": "Guru",`
  * * `"friend": { },`
  * `"tags":`

    `[`

    * `{`

      * `"id": 0,`
      * `"name": "string"`

      `}`

    `],`

  * `"status": "available",`
  * `"petType": "string"`

  `}`

`]`

### New pet Webhook

Information about a new pet in the systems

**Request Body schema: application/json**

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">
        <p>object</p>
        <p>Categories this pet belongs to</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>name</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>The name given to a pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>photoUrls</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>Array of strings &lt;url&gt; &lt;= 20 items</p>
        <p>The list of URL to a cute photos featuring pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">friend</td>
      <td style="text-align:left">object Recursive</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Array of objects (Tag) non-empty</p>
        <p>Tags attached to the pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;available&quot; &quot;pending&quot; &quot;sold&quot;</p>
        <p>Pet status in the store</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">petType</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Type of a pet</p>
        <p>cat</p>
        <p>cat</p>
        <p>dog</p>
        <p>bee</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>huntingSkill</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>Default: &quot;lazy&quot;</p>
        <p>Enum: &quot;clueless&quot; &quot;lazy&quot; &quot;adventurous&quot; &quot;aggressive&quot;</p>
        <p>The measured skill for hunting</p>
      </td>
    </tr>
  </tbody>
</table>

####  Request samples

* Payload

Content type

application/json

`{`

* `"category":`

  `{`

  * `"name": "string",`
  * `"sub":`

    `{`

    * `"prop1": "string"`

    `}`

  `},`

* `"name": "Guru",`
* * `"friend": { },`
* * `"status": "available",`
* `"petType": "cat",`
* `"huntingSkill": "adventurous"`

`}`

Access to Petstore orders

### Returns pet inventories by status

Returns a map of status codes to quantities

Default server

https://petstore.swagger.io/v2/store/inventory

Sandbox server

https://petstore.swagger.io/sandbox/store/inventory

####  Response samples

* 200

Content type

application/json

`{`

* `"property1": 0,`
* `"property2": 0`

`}`

### Place an order for a pet

**Request Body schema: application/json**

order placed for purchasing the pet

<table>
  <thead>
    <tr>
      <th style="text-align:left">quantity</th>
      <th style="text-align:left">
        <p>integer &lt;int32&gt; &gt;= 1</p>
        <p>Default: 1</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">shipDate</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;placed&quot; &quot;approved&quot; &quot;delivered&quot;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">requestId</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/store/order

Sandbox server

https://petstore.swagger.io/sandbox/store/order

####  Request samples

* Payload

Content type

application/json

`{`

* `"quantity": 1,`
* `"shipDate": "2019-08-24T14:15:22Z",`
* `"status": "placed",`
* `"requestId": "string"`

`}`

####  Response samples

* 200
* 400

Content type

application/json

application/xml

`{`

* `"id": 0,`
* `"petId": 0,`
* `"quantity": 1,`
* `"shipDate": "2019-08-24T14:15:22Z",`
* `"status": "placed",`
* `"complete": false`

`}`

### Find purchase order by ID

For valid response try integer IDs with value &lt;= 5 or &gt; 10. Other values will generated exceptions

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>orderId</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>integer &lt;int64&gt; [ 1 .. 5 ]</p>
        <p>ID of pet that needs to be fetched</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/store/order/{orderId}

Sandbox server

https://petstore.swagger.io/sandbox/store/order/{orderId}

####  Response samples

* 200

Content type

application/json

application/xml

`{`

* `"id": 0,`
* `"petId": 0,`
* `"quantity": 1,`
* `"shipDate": "2019-08-24T14:15:22Z",`
* `"status": "placed",`
* `"complete": false`

`}`

### Delete purchase order by ID

For valid response try integer IDs with value &lt; 1000. Anything above 1000 or nonintegers will generate API errors

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>orderId</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>string &gt;= 1</p>
        <p>ID of the order that needs to be deleted</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/store/order/{orderId}

Sandbox server

https://petstore.swagger.io/sandbox/store/order/{orderId}

### Subscribe to the Store events

Add subscription for a store events

**Request Body schema: application/json**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>callbackUrl</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>string &lt;uri&gt;</p>
        <p>This URL will be called by the server when the desired event will occur</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>eventName</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;orderInProgress&quot; &quot;orderShipped&quot; &quot;orderDelivered&quot;</p>
        <p>Event name for the subscription</p>
      </td>
    </tr>
  </tbody>
</table>

####  Callbacks

post

Order in Progress \(Summary\)

put

Order in Progress \(Only Description\)

post

Very long description Lorem ipsum dolor sit amet,

post

Order delivered Deprecated

Default server

https://petstore.swagger.io/v2/store/subscribe

Sandbox server

https://petstore.swagger.io/sandbox/store/subscribe

####  Request samples

* Payload

Content type

application/json

`{`

* * `"eventName": "orderInProgress"`

`}`

####  Response samples

* 201

Content type

application/json

`{`

* `"subscriptionId": "AAA-123-BBB-456"`

`}`

####  Callback payload samples

Callback

POST: Order in Progress \(Summary\)

POST: Order in Progress \(Summary\)

PUT: Order in Progress \(Only Description\)

POST: Very long description Lorem ipsum dolor sit amet,

POST: Order delivered

Content type

application/json

application/xml

`{`

* `"orderId": "123",`
* `"timestamp": "2018-10-19T16:46:45Z",`
* `"status": "inProgress"`

`}`

### Create user

This can only be done by the logged in user.

**Request Body schema: application/json**

Created user object

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Pet (object) or Tag (object)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">username</td>
      <td style="text-align:left">
        <p>string &gt;= 4 characters</p>
        <p>User supplied username</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">firstName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User first name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lastName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User last name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">email</td>
      <td style="text-align:left">
        <p>string &lt;email&gt;</p>
        <p>User email address</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">password</td>
      <td style="text-align:left">
        <p>string &lt;password&gt; &gt;= 8 characters /(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])/</p>
        <p>User password, MUST contain a mix of upper and lower case letters, as
          well as digits</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">phone</td>
      <td style="text-align:left">
        <p>string /^\+(?:[0-9]-?){6,14}[0-9]$/</p>
        <p>User phone number in international format</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">userStatus</td>
      <td style="text-align:left">
        <p>integer &lt;int32&gt;</p>
        <p>User status</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/user

Sandbox server

https://petstore.swagger.io/sandbox/user

####  Request samples

* Payload

Content type

application/json

`{`

* `"pet":`

  `{`

  * `"category":`

    `{`

    * `"name": "string",`
    * `"sub":`

      `{`

      * `"prop1": "string"`

      `}`

    `},`

  * `"name": "Guru",`
  * * `"friend": { },`
  * * `"status": "available",`
  * `"petType": "string"`

  `},`

* `"username": "John78",`
* `"firstName": "John",`
* `"lastName": "Smith",`
* `"email": "john.smith@example.com",`
* `"password": "drowssaP123",`
* `"phone": "+1-202-555-0192",`
* `"userStatus": 0`

`}`

### Get user by user name

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>username</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>string</p>
        <p>The name that needs to be fetched. Use user1 for testing.</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/{username}

Sandbox server

https://petstore.swagger.io/sandbox/user/{username}

####  Response samples

* 200

Content type

application/json

application/xml

`{`

* `"id": 0,`
* `"pet":`

  `{`

  * `"id": 0,`
  * `"category":`

    `{`

    * `"id": 0,`
    * `"name": "string",`
    * `"sub":`

      `{`

      * `"prop1": "string"`

      `}`

    `},`

  * `"name": "Guru",`
  * * `"friend": { },`
  * `"tags":`

    `[`

    * `{`

      * `"id": 0,`
      * `"name": "string"`

      `}`

    `],`

  * `"status": "available",`
  * `"petType": "string"`

  `},`

* `"username": "John78",`
* `"firstName": "John",`
* `"lastName": "Smith",`
* `"email": "john.smith@example.com",`
* `"password": "drowssaP123",`
* `"phone": "+1-202-555-0192",`
* `"userStatus": 0`

`}`

### Updated user

This can only be done by the logged in user.

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>username</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>string</p>
        <p>name that need to be deleted</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

**Request Body schema: application/json**

Updated user object

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Pet (object) or Tag (object)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">username</td>
      <td style="text-align:left">
        <p>string &gt;= 4 characters</p>
        <p>User supplied username</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">firstName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User first name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lastName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User last name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">email</td>
      <td style="text-align:left">
        <p>string &lt;email&gt;</p>
        <p>User email address</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">password</td>
      <td style="text-align:left">
        <p>string &lt;password&gt; &gt;= 8 characters /(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])/</p>
        <p>User password, MUST contain a mix of upper and lower case letters, as
          well as digits</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">phone</td>
      <td style="text-align:left">
        <p>string /^\+(?:[0-9]-?){6,14}[0-9]$/</p>
        <p>User phone number in international format</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">userStatus</td>
      <td style="text-align:left">
        <p>integer &lt;int32&gt;</p>
        <p>User status</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/{username}

Sandbox server

https://petstore.swagger.io/sandbox/user/{username}

####  Request samples

* Payload

Content type

application/json

`{`

* `"pet":`

  `{`

  * `"category":`

    `{`

    * `"name": "string",`
    * `"sub":`

      `{`

      * `"prop1": "string"`

      `}`

    `},`

  * `"name": "Guru",`
  * * `"friend": { },`
  * * `"status": "available",`
  * `"petType": "string"`

  `},`

* `"username": "John78",`
* `"firstName": "John",`
* `"lastName": "Smith",`
* `"email": "john.smith@example.com",`
* `"password": "drowssaP123",`
* `"phone": "+1-202-555-0192",`
* `"userStatus": 0`

`}`

### Delete user

This can only be done by the logged in user.

**path Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>username</p>
        <p>required</p>
      </th>
      <th style="text-align:left">
        <p>string</p>
        <p>The name that needs to be deleted</p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/{username}

Sandbox server

https://petstore.swagger.io/sandbox/user/{username}

### Creates list of users with given input array

**Request Body schema: application/json**

List of user object

 Array \(\)

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Pet (object) or Tag (object)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">username</td>
      <td style="text-align:left">
        <p>string &gt;= 4 characters</p>
        <p>User supplied username</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">firstName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User first name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lastName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User last name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">email</td>
      <td style="text-align:left">
        <p>string &lt;email&gt;</p>
        <p>User email address</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">password</td>
      <td style="text-align:left">
        <p>string &lt;password&gt; &gt;= 8 characters /(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])/</p>
        <p>User password, MUST contain a mix of upper and lower case letters, as
          well as digits</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">phone</td>
      <td style="text-align:left">
        <p>string /^\+(?:[0-9]-?){6,14}[0-9]$/</p>
        <p>User phone number in international format</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">userStatus</td>
      <td style="text-align:left">
        <p>integer &lt;int32&gt;</p>
        <p>User status</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/createWithArray

Sandbox server

https://petstore.swagger.io/sandbox/user/createWithArray

####  Request samples

* Payload

Content type

application/json

`[`

* `{`

  * `"pet":`

    `{`

    * `"category":`

      `{`

      * `"name": "string",`
      * `"sub":`

        `{`

        * `"prop1": "string"`

        `}`

      `},`

    * `"name": "Guru",`
    * * `"friend": { },`
    * * `"status": "available",`
    * `"petType": "string"`

    `},`

  * `"username": "John78",`
  * `"firstName": "John",`
  * `"lastName": "Smith",`
  * `"email": "john.smith@example.com",`
  * `"password": "drowssaP123",`
  * `"phone": "+1-202-555-0192",`
  * `"userStatus": 0`

  `}`

`]`

### Creates list of users with given input array

**Request Body schema: application/json**

List of user object

 Array \(\)

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Pet (object) or Tag (object)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">username</td>
      <td style="text-align:left">
        <p>string &gt;= 4 characters</p>
        <p>User supplied username</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">firstName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User first name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lastName</td>
      <td style="text-align:left">
        <p>string non-empty</p>
        <p>User last name</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">email</td>
      <td style="text-align:left">
        <p>string &lt;email&gt;</p>
        <p>User email address</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">password</td>
      <td style="text-align:left">
        <p>string &lt;password&gt; &gt;= 8 characters /(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])/</p>
        <p>User password, MUST contain a mix of upper and lower case letters, as
          well as digits</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">phone</td>
      <td style="text-align:left">
        <p>string /^\+(?:[0-9]-?){6,14}[0-9]$/</p>
        <p>User phone number in international format</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">userStatus</td>
      <td style="text-align:left">
        <p>integer &lt;int32&gt;</p>
        <p>User status</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/createWithList

Sandbox server

https://petstore.swagger.io/sandbox/user/createWithList

####  Request samples

* Payload

Content type

application/json

`[`

* `{`

  * `"pet":`

    `{`

    * `"category":`

      `{`

      * `"name": "string",`
      * `"sub":`

        `{`

        * `"prop1": "string"`

        `}`

      `},`

    * `"name": "Guru",`
    * * `"friend": { },`
    * * `"status": "available",`
    * `"petType": "string"`

    `},`

  * `"username": "John78",`
  * `"firstName": "John",`
  * `"lastName": "Smith",`
  * `"email": "john.smith@example.com",`
  * `"password": "drowssaP123",`
  * `"phone": "+1-202-555-0192",`
  * `"userStatus": 0`

  `}`

`]`

### Logs user into the system

**query Parameters**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>username</p>
        <p>required</p>
      </th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>password</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>The password for login in clear text</p>
      </td>
    </tr>
  </tbody>
</table>

Default server

https://petstore.swagger.io/v2/user/login

Sandbox server

https://petstore.swagger.io/sandbox/user/login

####  Response samples

* 200

Content type

application/json

application/xml

text/plain

### Logs out current logged in user session

Default server

https://petstore.swagger.io/v2/user/logout

Sandbox server

https://petstore.swagger.io/sandbox/user/logout

<table>
  <thead>
    <tr>
      <th style="text-align:left">id</th>
      <th style="text-align:left">
        <p>integer &lt;int64&gt;</p>
        <p>Pet ID</p>
        <p><a href="https://example.com/">Find more info here</a>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>object</p>
        <p>Categories this pet belongs to</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>name</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>The name given to a pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>photoUrls</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>Array of strings &lt;url&gt; &lt;= 20 items</p>
        <p>The list of URL to a cute photos featuring pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">friend</td>
      <td style="text-align:left">object Recursive</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Array of objects (Tag) non-empty</p>
        <p>Tags attached to the pet</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;available&quot; &quot;pending&quot; &quot;sold&quot;</p>
        <p>Pet status in the store</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">petType</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Type of a pet</p>
        <p>cat</p>
        <p>cat</p>
        <p>dog</p>
        <p>bee</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>huntingSkill</p>
        <p>required</p>
      </td>
      <td style="text-align:left">
        <p>string</p>
        <p>Default: &quot;lazy&quot;</p>
        <p>Enum: &quot;clueless&quot; &quot;lazy&quot; &quot;adventurous&quot; &quot;aggressive&quot;</p>
        <p>The measured skill for hunting</p>
      </td>
    </tr>
  </tbody>
</table>

`{`

* `"id": 0,`
* `"category":`

  `{`

  * `"id": 0,`
  * `"name": "string",`
  * `"sub":`

    `{`

    * `"prop1": "string"`

    `}`

  `},`

* `"name": "Guru",`
* * `"friend": { },`
* `"tags":`

  `[`

  * `{`

    * `"id": 0,`
    * `"name": "string"`

    `}`

  `],`

* `"status": "available",`
* `"petType": "cat",`
* `"huntingSkill": "adventurous"`

`}`

<table>
  <thead>
    <tr>
      <th style="text-align:left">id</th>
      <th style="text-align:left">
        <p>integer &lt;int64&gt;</p>
        <p>Order ID</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">petId</td>
      <td style="text-align:left">
        <p>integer &lt;int64&gt;</p>
        <p>Pet ID</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">quantity</td>
      <td style="text-align:left">
        <p>integer &lt;int32&gt; &gt;= 1</p>
        <p>Default: 1</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">shipDate</td>
      <td style="text-align:left">
        <p>string &lt;date-time&gt;</p>
        <p>Estimated ship date</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Enum: &quot;placed&quot; &quot;approved&quot; &quot;delivered&quot;</p>
        <p>Order Status</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">complete</td>
      <td style="text-align:left">
        <p>boolean</p>
        <p>Default: false</p>
        <p>Indicates whenever order was completed or not</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">requestId</td>
      <td style="text-align:left">
        <p>string</p>
        <p>Unique Request Id</p>
      </td>
    </tr>
  </tbody>
</table>

`{`

* `"quantity": 1,`
* `"shipDate": "2018-10-19T16:46:45Z",`
* `"status": "placed",`
* `"complete": false`

`}`

