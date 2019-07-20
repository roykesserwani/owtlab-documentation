---
title: Owtlab Restful API
language_tabs:
  - ruby: Ruby
  - python: Python
  - php: Php
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2

---

<h1 id="owtlab-restful-api">Owtlab Restful API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Resftul API documentation to integrate owtlab with your application.

Base URLs:

* <a href="https://owtlab.com/v1">https://owtlab.com/v1</a>

Email: <a href="mailto:support@owtlab.com">Support</a> 

# Authentication

* API Key (ApiKeyAuth)
    - Parameter Name: **api_key**, in: query. 

<h1 id="owtlab-restful-api-business">Business</h1>

A business profile belongs to a user.

## In order to create a business, a valid user id must exist in the database.

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://owtlab.com/v1/api/business',
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

r = requests.post('https://owtlab.com/v1/api/business', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://owtlab.com/v1/api/business', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

`POST /api/business`

> Body parameter

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="in-order-to-create-a-business,-a-valid-user-id-must-exist-in-the-database.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Business](#schemabusiness)|true|none|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="in-order-to-create-a-business,-a-valid-user-id-must-exist-in-the-database.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Business Object Response|[Business](#schemabusiness)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## Delete a business by a businessId.

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete 'https://owtlab.com/v1/api/business/{businessId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('https://owtlab.com/v1/api/business/{businessId}', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://owtlab.com/v1/api/business/{businessId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

`DELETE /api/business/{businessId}`

<h3 id="delete-a-business-by-a-businessid.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|businessId|path|integer|true|Numeric ID of business to delete|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="delete-a-business-by-a-businessid.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Business Object Response|[Business](#schemabusiness)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## Fetch a business by a businessId.

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://owtlab.com/v1/api/business/{businessId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://owtlab.com/v1/api/business/{businessId}', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://owtlab.com/v1/api/business/{businessId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

`GET /api/business/{businessId}`

<h3 id="fetch-a-business-by-a-businessid.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|businessId|path|integer|true|Numeric ID of business to update|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="fetch-a-business-by-a-businessid.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Business Object Response|[Business](#schemabusiness)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

## Update business information by business id.

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put 'https://owtlab.com/v1/api/business/{businessId}',
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

r = requests.put('https://owtlab.com/v1/api/business/{businessId}', params={

}, headers = headers)

print r.json()

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://owtlab.com/v1/api/business/{businessId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

`PUT /api/business/{businessId}`

> Body parameter

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="update-business-information-by-business-id.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|businessId|path|integer|true|Numeric ID of business to update|
|body|body|object|true|none|
|» name|body|string|false|none|
|» user_id|body|integer|false|none|

> Example responses

> 200 Response

```json
{
  "name": "string",
  "user_id": 0
}
```

<h3 id="update-business-information-by-business-id.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Business Object Response|[Business](#schemabusiness)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyAuth
</aside>

# Schemas

<h2 id="tocSbusiness">Business</h2>

<a id="schemabusiness"></a>

```json
{
  "name": "string",
  "user_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|user_id|integer|false|none|none|

