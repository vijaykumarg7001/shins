---
title: Event Management
language_tabs:
  - ruby: Ruby
  - python: Python
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2

---

<h1 id="event-management">Event Management v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is API server for EventManagement Project.

Base URLs:

* <a href="https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0">https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0</a>

* <a href="http://localhost:3000/v1/">http://localhost:3000/v1/</a>

Email: <a href="mailto:vijaykumarg7001@gmail.com">Support</a> 
License: <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache 2.0</a>

# Authentication

- HTTP Authentication, scheme: bearer 

- HTTP Authentication, scheme: bearer 

<h1 id="event-management-adminuser">adminUser</h1>

Admin Users

## Logs admin user into the system

<a id="opIdloginAdminUser"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/loginAdmin',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/loginAdmin', params={

}, headers = headers)

print r.json()

```

`POST /loginAdmin`

> Body parameter

```json
{
  "username": "admin",
  "password": "admin"
}
```

<h3 id="logs-admin-user-into-the-system-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» username|body|string|false|none|
|» password|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "token": "asdfasdfsadfsadfsafgd",
  "expiresIn": "1h",
  "userId": 1
}
```

<h3 id="logs-admin-user-into-the-system-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid username/password supplied|Inline|

<h3 id="logs-admin-user-into-the-system-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» token|string|false|none|none|
|» expiresIn|string|false|none|none|
|» userId|integer(int64)|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="event-management-user">user</h1>

Users

## Logs user into the system

<a id="opIdloginUser"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/loginUser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/loginUser', params={

}, headers = headers)

print r.json()

```

`POST /loginUser`

> Body parameter

```json
{
  "email": "admin",
  "password": "admin"
}
```

<h3 id="logs-user-into-the-system-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» email|body|string|false|none|
|» password|body|string|false|none|

> Example responses

> 200 Response

```json
{
  "message": "Successfully logged in",
  "token": "asdfasdfsadfsadfsafgd"
}
```

<h3 id="logs-user-into-the-system-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid username/password supplied|Inline|

<h3 id="logs-user-into-the-system-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|
|» token|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="event-management-organizations">organizations</h1>

Organizations here

## Get all the Organizations

<a id="opIdgetOrganizations"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations', params={

}, headers = headers)

print r.json()

```

`GET /organizations`

Returns an array of all the Organizations

> Example responses

> 200 Response

```json
{
  "message": "Organizations fetched successfully",
  "organizations": [
    {
      "id": 0,
      "name": "TVAsia",
      "CreatedBy": {
        "id": 1,
        "name": "Admin User"
      }
    }
  ]
}
```

<h3 id="get-all-the-organizations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|[OrganizationResponse](#schemaorganizationresponse)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Access token is missing or invalid for admin login|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|AdminUserID not found|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
admin_auth
</aside>

## Add a new organization

<a id="opIdaddOrganization"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations', params={

}, headers = headers)

print r.json()

```

`POST /organizations`

> Body parameter

```json
{
  "name": "TVAsia"
}
```

<h3 id="add-a-new-organization-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Organization](#schemaorganization)|true|Organization object that needs to be added|

> Example responses

> 201 Response

```json
{
  "message": "Organization Added Successfully",
  "organization": {
    "id": 1
  }
}
```

<h3 id="add-a-new-organization-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|successfully added|[OrganizationCreateResponse](#schemaorganizationcreateresponse)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Access token is missing or invalid for admin login|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Email already exists|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
admin_auth
</aside>

## Update an existing organization

<a id="opIdupdateOrganization"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.put 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.put('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}', params={

}, headers = headers)

print r.json()

```

`PUT /organizations/{organizationId}`

> Body parameter

```json
{
  "name": "TVAsia"
}
```

<h3 id="update-an-existing-organization-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|ID of Organization to update|
|body|body|[Organization](#schemaorganization)|true|Organization object that needs to be added|

<h3 id="update-an-existing-organization-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successfully updated|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Access token is missing or invalid for admin login|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|OrganizationID not found|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|
|409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|Email already exists|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
admin_auth
</aside>

## Get Organization info by ID

<a id="opIdgetOrganizationById"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}', params={

}, headers = headers)

print r.json()

```

`GET /organizations/{organizationId}`

Returns a single Organization

<h3 id="get-organization-info-by-id-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|ID of Organization to return|

> Example responses

> 200 Response

```json
{
  "message": "Organizations fetched successfully",
  "organizations": [
    {
      "id": 0,
      "name": "TVAsia",
      "CreatedBy": {
        "id": 1,
        "name": "Admin User"
      }
    }
  ]
}
```

<h3 id="get-organization-info-by-id-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|[OrganizationResponse](#schemaorganizationresponse)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Access token is missing or invalid for admin login|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|OrganizationID not found|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
admin_auth
</aside>

## Deletes an Organization

<a id="opIddeleteOrganization"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.delete 'https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Authorization': 'Bearer {access-token}'
}

r = requests.delete('https://virtserver.swaggerhub.com/vijaykumarg7001/event_management/1.0.0/organizations/{organizationId}', params={

}, headers = headers)

print r.json()

```

`DELETE /organizations/{organizationId}`

Delete an Organization by its ID

<h3 id="deletes-an-organization-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|organizationId|path|string|true|ID of Organization to return|

<h3 id="deletes-an-organization-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Access token is missing or invalid for admin login|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|OrganizationID not found|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
admin_auth
</aside>

# Schemas

<h2 id="tocSadminuser">AdminUser</h2>

<a id="schemaadminuser"></a>

```json
{
  "id": 0,
  "username": "string",
  "password": "string",
  "comments": "string",
  "userStatus": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|username|string|false|none|none|
|password|string|false|none|none|
|comments|string|false|none|none|
|userStatus|integer(int32)|false|none|User Status|

<h2 id="tocSuser">User</h2>

<a id="schemauser"></a>

```json
{
  "id": 0,
  "email": "string",
  "password": "string",
  "organizationId": 0,
  "userType": 0,
  "firstName": "string",
  "lastName": "string",
  "phone": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|email|string|true|none|none|
|password|string|true|none|none|
|organizationId|integer(int64)|false|none|none|
|userType|integer(int32)|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|phone|string|false|none|none|

<h2 id="tocSorganization">Organization</h2>

<a id="schemaorganization"></a>

```json
{
  "id": 0,
  "name": "TVAsia"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|name|string|false|none|none|

<h2 id="tocSorganizationcreateresponse">OrganizationCreateResponse</h2>

<a id="schemaorganizationcreateresponse"></a>

```json
{
  "message": "Organization Added Successfully",
  "organization": {
    "id": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|false|none|none|
|organization|object|false|none|none|
|» id|integer(int64)|false|none|none|

<h2 id="tocSorganizationresponse">OrganizationResponse</h2>

<a id="schemaorganizationresponse"></a>

```json
{
  "message": "Organizations fetched successfully",
  "organizations": [
    {
      "id": 0,
      "name": "TVAsia",
      "CreatedBy": {
        "id": 1,
        "name": "Admin User"
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|false|none|none|
|organizations|[object]|false|none|none|
|» id|integer(int64)|false|read-only|none|
|» name|string|false|none|none|
|» CreatedBy|object|false|none|none|
|»» id|integer(int64)|false|none|none|
|»» name|string|false|none|none|

<h2 id="tocSusertypes">UserTypes</h2>

<a id="schemausertypes"></a>

```json
{
  "id": 0,
  "description": "TVAsia"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|description|string|false|none|none|

<h2 id="tocSuseracl">UserACL</h2>

<a id="schemauseracl"></a>

```json
{
  "id": 0,
  "aclName": "Create Events"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|aclName|string|false|none|none|

<h2 id="tocSusertypeacl">UserTypeACL</h2>

<a id="schemausertypeacl"></a>

```json
{
  "id": 0,
  "userTypeId": 0,
  "aclId": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|userTypeId|integer(int64)|false|none|none|
|aclId|integer(int64)|false|none|none|

