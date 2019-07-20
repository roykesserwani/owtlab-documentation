---
title: Owtlab Restful API
language_tabs:
  - ruby: Ruby
  - python: Python
toc_footers: []
includes: []
search: true
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

- oAuth2 authentication. 

    - Flow: implicit
    - Authorization URL = [https://google.com](https://google.com)

|Scope|Scope Description|
|---|---|

<h1 id="owtlab-restful-api-bank-validation">Bank Validation</h1>

## Validate routing and account number

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://owtlab.com/v1/bank/validate',
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

r = requests.post('https://owtlab.com/v1/bank/validate', params={

}, headers = headers)

print r.json()

```

`POST /bank/validate`

> Body parameter

```json
{
  "routing": 0,
  "account": "string"
}
```

<h3 id="validate-routing-and-account-number-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Bank](#schemabank)|true|Bank Object|

> Example responses

> 200 Response

```json
{
  "routing": 0,
  "account": "string"
}
```

<h3 id="validate-routing-and-account-number-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful validation response|[Bank](#schemabank)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocSbank">Bank</h2>

<a id="schemabank"></a>

```json
{
  "routing": 0,
  "account": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|routing|integer|false|none|none|
|account|string|false|none|none|

