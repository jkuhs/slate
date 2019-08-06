---
title: ReactorOne API
language_tabs:
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - java: Java
toc_footers:
  - '<a href="https://www.reactorone.com">Find out more about ReactorOne</a>'
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="reactorone-api">ReactorOne API v2.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The official ReactorOne REST API.

Base URLs:

* <a href="https://dev-api.reactorone.net/api/2">https://dev-api.reactorone.net/api/2</a>

Email: <a href="mailto:contact@reactorone.com">Support</a> 

# Authentication

* API Key (psk)
    - Parameter Name: **X-REACTORONE-PSK**, in: header. 

* API Key (tenant)
    - Parameter Name: **X-RO-TENANT**, in: header. 

<h1 id="reactorone-api-products">Products</h1>

Manage products

<a href="">External documentation</a>

## Get Products

<a id="opIdGet Products"></a>

> Code samples

```http
GET https://dev-api.reactorone.net/api/2/products HTTP/1.1
Host: dev-api.reactorone.net
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/products',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/products',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/products");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`GET /products`

*Retrieves a list of products*

<h3 id="get-products-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemIds|query|string|false|Return only products with matching item IDs|
|page|query|integer|false|Return results for a specific page.|
|size|query|integer|false|Return up to this many results per page. Maximum `250`|

> Example responses

> 200 Response

```json
[
  {
    "itemId": "string",
    "slug": "string",
    "title": "string",
    "description": "string",
    "summary": "string",
    "online": true,
    "metaTitle": "string",
    "metaDescription": "string",
    "metaKeywords": "string",
    "masterSku": "string",
    "skus": [
      {
        "id": 0,
        "itemId": "string",
        "productId": "string",
        "slug": "string",
        "title": "string",
        "description": "string",
        "collection": "string",
        "type": "string",
        "subType": "string",
        "status": "string",
        "arrivalDate": 0,
        "eta": 0,
        "popularityIndex": 0,
        "online = true": true,
        "discontinued": true,
        "gender": "string",
        "metaTitle": "string",
        "metaDescription": "string",
        "metaKeywords": "string",
        "brandName": "string",
        "seller": "string",
        "manufacturerCode": "string",
        "manufacturerName": "string",
        "madeInCountry": "string",
        "upc": "string",
        "costPrice": 0,
        "basePrice": 0,
        "adjustedPrice": 0,
        "salePrice": 0,
        "currencyCode": "string",
        "quantityAvailable": 0,
        "quantityIncrement": 0,
        "uom": "string",
        "weight": 0,
        "weightUnit": "string",
        "width": 0,
        "widthUnit": "string",
        "length": 0,
        "lengthUnit": "string",
        "height": 0,
        "heightUnit": "string",
        "depth": 0,
        "depthUnit": "string",
        "volume": 0,
        "volumeUnit": "string",
        "customAttributes": {},
        "images": [
          0
        ],
        "relatedProducts": [
          0
        ],
        "crossSells": [
          0
        ],
        "upSells": [
          0
        ],
        "tags": [
          "string"
        ],
        "features": [
          "string"
        ],
        "itemPromotions": [
          0
        ],
        "productBundlePromotions": [
          0
        ],
        "directRestrictions": [
          "string"
        ],
        "userSegmentationBlacklist": [
          "string"
        ],
        "userSegmentationWhitelist": [
          "string"
        ],
        "primaryCategory": 0,
        "backorderable": true,
        "removeWhenOutOfStock": true,
        "taxCode": "string",
        "lastSyncDate": 0,
        "createdDate": 0,
        "lastModifiedDate": 0
      }
    ],
    "images": [
      {
        "id": 0,
        "gid": "string",
        "displayName": "string",
        "description": "string",
        "slug": "string",
        "tags": [
          "string"
        ],
        "filename": "string",
        "filePath": "string",
        "externalUrl": "string",
        "externalStorage": "string",
        "originalFilename": "string",
        "mediaType": "string",
        "extension": "string",
        "size": 0,
        "altText": "string",
        "md5Checksum": "string",
        "locale": "string",
        "url": "string",
        "type": "string",
        "view": "string",
        "width": 0,
        "height": 0,
        "quality": 0,
        "thumbnail": "string"
      }
    ],
    "variationAttributes": [
      "string"
    ],
    "tags": [
      "string"
    ],
    "customProductAttributes": {},
    "searchKeywords": [
      {
        "input": "string",
        "weight": 0
      }
    ],
    "createdDate": 0,
    "lastModifiedDate": 0
  }
]
```

<h3 id="get-products-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|

<h3 id="get-products-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[Product](#schemaproduct)]|false|none|none|
|» itemId|string|true|none|Unique product ID.|
|» slug|string|false|none|Unique, human-friendly product identifier that is used in URLs. Generated from master SKU if not provided.|
|» title|string|false|none|The product title. Uses master SKU title if not provided.|
|» description|string|false|none|The product description (supports HTML). Uses master SKU description if not provided.|
|» summary|string|false|none|The product summary (supports HTML).|
|» online|boolean|false|none|Indicates whether the product is online. Defaults to `true`.|
|» metaTitle|string|false|none|The title of the product used for SEO purposes. Generally added to the `<meta name='title'>` tag. Uses `title` if not provided.|
|» metaDescription|string|false|none|The description of the product used for SEO purposes. Generally added to the `<meta name='description'>` tag Uses `description` if not provided|
|» metaKeywords|string|false|none|The keywords of the product used for SEO purposes. Generally added to the `<meta name='keywords'>` tag.|
|» masterSku|string|false|none|The `itemId` of the master/primary SKU.|
|» skus|[[Sku](#schemasku)]|false|none|New or existing SKUs associated with the product.|
|»» id|integer(int64)|false|read-only|none|
|»» itemId|string|false|none|Unique SKU item ID|
|»» productId|string|false|none|none|
|»» slug|string|false|none|Unique, human-friendly identifier that is used in URLs.|
|»» title|string|false|none|none|
|»» description|string|false|none|none|
|»» collection|string|false|none|none|
|»» type|string|false|none|none|
|»» subType|string|false|none|none|
|»» status|string|false|none|none|
|»» arrivalDate|integer(int64)|false|none|none|
|»» eta|integer(int64)|false|none|none|
|»» popularityIndex|integer|false|none|none|
|»» online = true|boolean|false|none|none|
|»» discontinued|boolean|false|none|none|
|»» gender|string|false|none|none|
|»» metaTitle|string|false|none|none|
|»» metaDescription|string|false|none|none|
|»» metaKeywords|string|false|none|none|
|»» brandName|string|false|none|none|
|»» seller|string|false|none|none|
|»» manufacturerCode|string|false|none|none|
|»» manufacturerName|string|false|none|none|
|»» madeInCountry|string|false|none|none|
|»» upc|string|false|none|none|
|»» costPrice|number|false|none|none|
|»» basePrice|number|false|none|none|
|»» adjustedPrice|number|false|none|none|
|»» salePrice|number|false|none|none|
|»» currencyCode|string|false|none|none|
|»» quantityAvailable|integer|false|none|none|
|»» quantityIncrement|integer|false|none|none|
|»» uom|string|false|none|none|
|»» weight|integer|false|none|none|
|»» weightUnit|string|false|none|none|
|»» width|integer|false|none|none|
|»» widthUnit|string|false|none|none|
|»» length|integer|false|none|none|
|»» lengthUnit|string|false|none|none|
|»» height|integer|false|none|none|
|»» heightUnit|string|false|none|none|
|»» depth|integer|false|none|none|
|»» depthUnit|string|false|none|none|
|»» volume|integer|false|none|none|
|»» volumeUnit|string|false|none|none|
|»» customAttributes|object|false|none|none|
|»» images|[integer]|false|none|none|
|»» relatedProducts|[integer]|false|none|none|
|»» crossSells|[integer]|false|none|none|
|»» upSells|[integer]|false|none|none|
|»» tags|[string]|false|none|none|
|»» features|[string]|false|none|none|
|»» itemPromotions|[integer]|false|none|none|
|»» productBundlePromotions|[integer]|false|none|none|
|»» directRestrictions|[string]|false|none|none|
|»» userSegmentationBlacklist|[string]|false|none|none|
|»» userSegmentationWhitelist|[string]|false|none|none|
|»» primaryCategory|integer(int64)|false|none|none|
|»» backorderable|boolean|false|none|none|
|»» removeWhenOutOfStock|boolean|false|none|none|
|»» taxCode|string|false|none|none|
|»» lastSyncDate|integer(int64)|false|none|none|
|»» createdDate|integer(int64)|false|read-only|none|
|»» lastModifiedDate|integer(int64)|false|read-only|none|
|» images|[[Image](#schemaimage)]|false|none|New or existing images associated with the product.|
|»» id|integer|false|none|none|
|»» gid|string|false|none|none|
|»» displayName|string|false|none|none|
|»» description|string|false|none|none|
|»» slug|string|false|none|none|
|»» tags|[string]|false|none|none|
|»» filename|string|true|none|none|
|»» filePath|string|false|none|none|
|»» externalUrl|string|true|none|none|
|»» externalStorage|string|false|none|none|
|»» originalFilename|string|false|none|none|
|»» mediaType|string|false|none|none|
|»» extension|string|false|none|none|
|»» size|integer|false|none|Image file size in bytes|
|»» altText|string|false|none|none|
|»» md5Checksum|string|false|none|none|
|»» locale|string|false|none|none|
|»» url|string|false|none|none|
|»» type|string|false|none|none|
|»» view|string|false|none|none|
|»» width|integer|false|none|The image width in pixels|
|»» height|integer|false|none|The image height in pixels|
|»» quality|integer|false|none|The image quality (1-100)|
|»» thumbnail|string|false|none|none|
|» variationAttributes|[string]|false|none|Variation attributes to be used for the product (e.g. `color`, `size`).|
|» tags|[string]|false|none|none|
|» customProductAttributes|object|false|none|Custom product attributes provided as key-value pairs. Both keys and values must be strings.|
|» searchKeywords|[[SearchKeyword](#schemasearchkeyword)]|false|none|Search keywords to be used in the product search.|
|»» input|string|false|none|The search keyword.|
|»» weight|integer|false|none|The search weight of the keyword.|
|» createdDate|integer(int64)|false|read-only|none|
|» lastModifiedDate|integer(int64)|false|read-only|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

## Create_Update Products

<a id="opIdCreate/Update Products"></a>

> Code samples

```http
POST https://dev-api.reactorone.net/api/2/products HTTP/1.1
Host: dev-api.reactorone.net
Content-Type: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/products',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "itemId": "string",
  "slug": "string",
  "title": "string",
  "description": "string",
  "summary": "string",
  "online": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "masterSku": "string",
  "skus": [
    {
      "itemId": "string",
      "productId": "string",
      "slug": "string",
      "title": "string",
      "description": "string",
      "collection": "string",
      "type": "string",
      "subType": "string",
      "status": "string",
      "arrivalDate": 0,
      "eta": 0,
      "popularityIndex": 0,
      "online = true": true,
      "discontinued": true,
      "gender": "string",
      "metaTitle": "string",
      "metaDescription": "string",
      "metaKeywords": "string",
      "brandName": "string",
      "seller": "string",
      "manufacturerCode": "string",
      "manufacturerName": "string",
      "madeInCountry": "string",
      "upc": "string",
      "costPrice": 0,
      "basePrice": 0,
      "adjustedPrice": 0,
      "salePrice": 0,
      "currencyCode": "string",
      "quantityAvailable": 0,
      "quantityIncrement": 0,
      "uom": "string",
      "weight": 0,
      "weightUnit": "string",
      "width": 0,
      "widthUnit": "string",
      "length": 0,
      "lengthUnit": "string",
      "height": 0,
      "heightUnit": "string",
      "depth": 0,
      "depthUnit": "string",
      "volume": 0,
      "volumeUnit": "string",
      "customAttributes": {},
      "images": [
        0
      ],
      "relatedProducts": [
        0
      ],
      "crossSells": [
        0
      ],
      "upSells": [
        0
      ],
      "tags": [
        "string"
      ],
      "features": [
        "string"
      ],
      "itemPromotions": [
        0
      ],
      "productBundlePromotions": [
        0
      ],
      "directRestrictions": [
        "string"
      ],
      "userSegmentationBlacklist": [
        "string"
      ],
      "userSegmentationWhitelist": [
        "string"
      ],
      "primaryCategory": 0,
      "backorderable": true,
      "removeWhenOutOfStock": true,
      "taxCode": "string",
      "lastSyncDate": 0
    }
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "variationAttributes": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "customProductAttributes": {},
  "searchKeywords": [
    {
      "input": "string",
      "weight": 0
    }
  ]
}';
const headers = {
  'Content-Type':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/products',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/products");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /products`

*Create new or update existing products*

> Body parameter

```json
{
  "itemId": "string",
  "slug": "string",
  "title": "string",
  "description": "string",
  "summary": "string",
  "online": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "masterSku": "string",
  "skus": [
    {
      "itemId": "string",
      "productId": "string",
      "slug": "string",
      "title": "string",
      "description": "string",
      "collection": "string",
      "type": "string",
      "subType": "string",
      "status": "string",
      "arrivalDate": 0,
      "eta": 0,
      "popularityIndex": 0,
      "online = true": true,
      "discontinued": true,
      "gender": "string",
      "metaTitle": "string",
      "metaDescription": "string",
      "metaKeywords": "string",
      "brandName": "string",
      "seller": "string",
      "manufacturerCode": "string",
      "manufacturerName": "string",
      "madeInCountry": "string",
      "upc": "string",
      "costPrice": 0,
      "basePrice": 0,
      "adjustedPrice": 0,
      "salePrice": 0,
      "currencyCode": "string",
      "quantityAvailable": 0,
      "quantityIncrement": 0,
      "uom": "string",
      "weight": 0,
      "weightUnit": "string",
      "width": 0,
      "widthUnit": "string",
      "length": 0,
      "lengthUnit": "string",
      "height": 0,
      "heightUnit": "string",
      "depth": 0,
      "depthUnit": "string",
      "volume": 0,
      "volumeUnit": "string",
      "customAttributes": {},
      "images": [
        0
      ],
      "relatedProducts": [
        0
      ],
      "crossSells": [
        0
      ],
      "upSells": [
        0
      ],
      "tags": [
        "string"
      ],
      "features": [
        "string"
      ],
      "itemPromotions": [
        0
      ],
      "productBundlePromotions": [
        0
      ],
      "directRestrictions": [
        "string"
      ],
      "userSegmentationBlacklist": [
        "string"
      ],
      "userSegmentationWhitelist": [
        "string"
      ],
      "primaryCategory": 0,
      "backorderable": true,
      "removeWhenOutOfStock": true,
      "taxCode": "string",
      "lastSyncDate": 0
    }
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "variationAttributes": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "customProductAttributes": {},
  "searchKeywords": [
    {
      "input": "string",
      "weight": 0
    }
  ]
}
```

<h3 id="create_update-products-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[Product](#schemaproduct)|false|none|

<h3 id="create_update-products-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

## Get SKUs

<a id="opIdGet SKUs"></a>

> Code samples

```http
GET https://dev-api.reactorone.net/api/2/product/skus HTTP/1.1
Host: dev-api.reactorone.net
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/product/skus',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/product/skus',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/product/skus");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`GET /product/skus`

*Retrieves a list of SKUs*

<h3 id="get-skus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemIds|query|string|false|Return only SKUs with matching item IDs|
|page|query|integer|false|Return results for a specific page.|
|size|query|integer|false|Return up to this many results per page. Maximum `250`|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "itemId": "string",
    "productId": "string",
    "slug": "string",
    "title": "string",
    "description": "string",
    "collection": "string",
    "type": "string",
    "subType": "string",
    "status": "string",
    "arrivalDate": 0,
    "eta": 0,
    "popularityIndex": 0,
    "online = true": true,
    "discontinued": true,
    "gender": "string",
    "metaTitle": "string",
    "metaDescription": "string",
    "metaKeywords": "string",
    "brandName": "string",
    "seller": "string",
    "manufacturerCode": "string",
    "manufacturerName": "string",
    "madeInCountry": "string",
    "upc": "string",
    "costPrice": 0,
    "basePrice": 0,
    "adjustedPrice": 0,
    "salePrice": 0,
    "currencyCode": "string",
    "quantityAvailable": 0,
    "quantityIncrement": 0,
    "uom": "string",
    "weight": 0,
    "weightUnit": "string",
    "width": 0,
    "widthUnit": "string",
    "length": 0,
    "lengthUnit": "string",
    "height": 0,
    "heightUnit": "string",
    "depth": 0,
    "depthUnit": "string",
    "volume": 0,
    "volumeUnit": "string",
    "customAttributes": {},
    "images": [
      0
    ],
    "relatedProducts": [
      0
    ],
    "crossSells": [
      0
    ],
    "upSells": [
      0
    ],
    "tags": [
      "string"
    ],
    "features": [
      "string"
    ],
    "itemPromotions": [
      0
    ],
    "productBundlePromotions": [
      0
    ],
    "directRestrictions": [
      "string"
    ],
    "userSegmentationBlacklist": [
      "string"
    ],
    "userSegmentationWhitelist": [
      "string"
    ],
    "primaryCategory": 0,
    "backorderable": true,
    "removeWhenOutOfStock": true,
    "taxCode": "string",
    "lastSyncDate": 0,
    "createdDate": 0,
    "lastModifiedDate": 0
  }
]
```

<h3 id="get-skus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|

<h3 id="get-skus-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[Sku](#schemasku)]|false|none|none|
|» id|integer(int64)|false|read-only|none|
|» itemId|string|false|none|Unique SKU item ID|
|» productId|string|false|none|none|
|» slug|string|false|none|Unique, human-friendly identifier that is used in URLs.|
|» title|string|false|none|none|
|» description|string|false|none|none|
|» collection|string|false|none|none|
|» type|string|false|none|none|
|» subType|string|false|none|none|
|» status|string|false|none|none|
|» arrivalDate|integer(int64)|false|none|none|
|» eta|integer(int64)|false|none|none|
|» popularityIndex|integer|false|none|none|
|» online = true|boolean|false|none|none|
|» discontinued|boolean|false|none|none|
|» gender|string|false|none|none|
|» metaTitle|string|false|none|none|
|» metaDescription|string|false|none|none|
|» metaKeywords|string|false|none|none|
|» brandName|string|false|none|none|
|» seller|string|false|none|none|
|» manufacturerCode|string|false|none|none|
|» manufacturerName|string|false|none|none|
|» madeInCountry|string|false|none|none|
|» upc|string|false|none|none|
|» costPrice|number|false|none|none|
|» basePrice|number|false|none|none|
|» adjustedPrice|number|false|none|none|
|» salePrice|number|false|none|none|
|» currencyCode|string|false|none|none|
|» quantityAvailable|integer|false|none|none|
|» quantityIncrement|integer|false|none|none|
|» uom|string|false|none|none|
|» weight|integer|false|none|none|
|» weightUnit|string|false|none|none|
|» width|integer|false|none|none|
|» widthUnit|string|false|none|none|
|» length|integer|false|none|none|
|» lengthUnit|string|false|none|none|
|» height|integer|false|none|none|
|» heightUnit|string|false|none|none|
|» depth|integer|false|none|none|
|» depthUnit|string|false|none|none|
|» volume|integer|false|none|none|
|» volumeUnit|string|false|none|none|
|» customAttributes|object|false|none|none|
|» images|[integer]|false|none|none|
|» relatedProducts|[integer]|false|none|none|
|» crossSells|[integer]|false|none|none|
|» upSells|[integer]|false|none|none|
|» tags|[string]|false|none|none|
|» features|[string]|false|none|none|
|» itemPromotions|[integer]|false|none|none|
|» productBundlePromotions|[integer]|false|none|none|
|» directRestrictions|[string]|false|none|none|
|» userSegmentationBlacklist|[string]|false|none|none|
|» userSegmentationWhitelist|[string]|false|none|none|
|» primaryCategory|integer(int64)|false|none|none|
|» backorderable|boolean|false|none|none|
|» removeWhenOutOfStock|boolean|false|none|none|
|» taxCode|string|false|none|none|
|» lastSyncDate|integer(int64)|false|none|none|
|» createdDate|integer(int64)|false|read-only|none|
|» lastModifiedDate|integer(int64)|false|read-only|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

## Create_Update SKUs

<a id="opIdCreate/Update SKUs"></a>

> Code samples

```http
POST https://dev-api.reactorone.net/api/2/product/skus HTTP/1.1
Host: dev-api.reactorone.net
Content-Type: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/product/skus',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "itemId": "string",
  "productId": "string",
  "title": "string",
  "slug": "string",
  "description": "string",
  "summary": "string",
  "collection": "string",
  "type": "string",
  "subType": "string",
  "status": "string",
  "popularityIndex": 0,
  "online": true,
  "discontinued": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "brandName": "string",
  "seller": "string",
  "manufacturerCode": "string",
  "manufacturerName": "string",
  "madeInCountry": "string",
  "upc": "string",
  "currencyCode": "string",
  "quantityAvailable": 0,
  "quantityIncrement": 0,
  "uom": "string",
  "weight": 0,
  "weightUnit": "string",
  "width": 0,
  "widthUnit": "string",
  "length": 0,
  "lengthUnit": "string",
  "height": 0,
  "heightUnit": "string",
  "depth": 0,
  "depthUnit": "string",
  "volume": 0,
  "volumeUnit": "string",
  "backorderable": true,
  "removeWhenOutOfStock": true,
  "costPrice": 0,
  "basePrice": 0,
  "adjustedPrice": 0,
  "salePrice": 0,
  "arrivalDate": 0,
  "eta": 0,
  "gender": "string",
  "taxCode": "string",
  "customAttributes": {},
  "features": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "fulfillmentProviders": [
    {
      "id": "string",
      "sku": {
        "itemId": "string",
        "quantityAvailable": 0,
        "online": true,
        "discontinued": true,
        "backorderable": true
      }
    }
  ]
}';
const headers = {
  'Content-Type':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/product/skus',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/product/skus");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /product/skus`

*Create new or update existing SKUs*

> Body parameter

```json
{
  "itemId": "string",
  "productId": "string",
  "title": "string",
  "slug": "string",
  "description": "string",
  "summary": "string",
  "collection": "string",
  "type": "string",
  "subType": "string",
  "status": "string",
  "popularityIndex": 0,
  "online": true,
  "discontinued": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "brandName": "string",
  "seller": "string",
  "manufacturerCode": "string",
  "manufacturerName": "string",
  "madeInCountry": "string",
  "upc": "string",
  "currencyCode": "string",
  "quantityAvailable": 0,
  "quantityIncrement": 0,
  "uom": "string",
  "weight": 0,
  "weightUnit": "string",
  "width": 0,
  "widthUnit": "string",
  "length": 0,
  "lengthUnit": "string",
  "height": 0,
  "heightUnit": "string",
  "depth": 0,
  "depthUnit": "string",
  "volume": 0,
  "volumeUnit": "string",
  "backorderable": true,
  "removeWhenOutOfStock": true,
  "costPrice": 0,
  "basePrice": 0,
  "adjustedPrice": 0,
  "salePrice": 0,
  "arrivalDate": 0,
  "eta": 0,
  "gender": "string",
  "taxCode": "string",
  "customAttributes": {},
  "features": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "fulfillmentProviders": [
    {
      "id": "string",
      "sku": {
        "itemId": "string",
        "quantityAvailable": 0,
        "online": true,
        "discontinued": true,
        "backorderable": true
      }
    }
  ]
}
```

<h3 id="create_update-skus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SkuImport](#schemaskuimport)|false|none|

<h3 id="create_update-skus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

<h1 id="reactorone-api-reports">Reports</h1>

Reports for various metrics and dimensions

## Request Report

<a id="opIdRequest Report"></a>

> Code samples

```http
POST https://dev-api.reactorone.net/api/2/reports HTTP/1.1
Host: dev-api.reactorone.net
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/reports',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "startDate": "2019-04-25T19:59:37Z",
  "endDate": "2019-04-25T19:59:37Z",
  "metrics": [
    {
      "name": "string",
      "dimensions": [
        "string"
      ]
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/reports',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/reports");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /reports`

*Request a report*

> Body parameter

```json
{
  "startDate": "2019-04-25T19:59:37Z",
  "endDate": "2019-04-25T19:59:37Z",
  "metrics": [
    {
      "name": "string",
      "dimensions": [
        "string"
      ]
    }
  ]
}
```

<h3 id="request-report-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ReportRequest](#schemareportrequest)|false|none|

> Example responses

> 200 Response

```json
{
  "startDate": "string",
  "endDate": "string",
  "metrics": [
    {
      "name": "string",
      "dimensions": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ]
}
```

<h3 id="request-report-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|[ReportResponse](#schemareportresponse)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

<h1 id="reactorone-api-orders">Orders</h1>

## Get Orders

<a id="opIdGet Orders"></a>

> Code samples

```http
GET https://dev-api.reactorone.net/api/2/orders HTTP/1.1
Host: dev-api.reactorone.net
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/orders',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/orders',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/orders");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`GET /orders`

*Retrieves a list of orders*

<h3 id="get-orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer(int64)|false|Return only orders with matching IDs.|
|since-id|query|integer(int64)|false|Return only orders after the specified ID.|
|since|query|integer(int64)|false|Return only orders after the specified date.|
|page|query|integer|false|Return results for a specific page.|
|size|query|integer|false|Return up to this many results per page. Maximum `250`|

> Example responses

> 200 Response

```json
[
  {
    "id": 0,
    "guid": "string",
    "extCartId": "string",
    "extSiteName": "string",
    "extSiteOrderId": "string",
    "extIntermediaryOrderId": "string",
    "orderItems": [
      {
        "uuid": "string",
        "sku": {
          "id": 0,
          "itemId": "string",
          "productId": "string",
          "slug": "string",
          "title": "string",
          "description": "string",
          "collection": "string",
          "type": "string",
          "subType": "string",
          "status": "string",
          "arrivalDate": 0,
          "eta": 0,
          "popularityIndex": 0,
          "online = true": true,
          "discontinued": true,
          "gender": "string",
          "metaTitle": "string",
          "metaDescription": "string",
          "metaKeywords": "string",
          "brandName": "string",
          "seller": "string",
          "manufacturerCode": "string",
          "manufacturerName": "string",
          "madeInCountry": "string",
          "upc": "string",
          "costPrice": 0,
          "basePrice": 0,
          "adjustedPrice": 0,
          "salePrice": 0,
          "currencyCode": "string",
          "quantityAvailable": 0,
          "quantityIncrement": 0,
          "uom": "string",
          "weight": 0,
          "weightUnit": "string",
          "width": 0,
          "widthUnit": "string",
          "length": 0,
          "lengthUnit": "string",
          "height": 0,
          "heightUnit": "string",
          "depth": 0,
          "depthUnit": "string",
          "volume": 0,
          "volumeUnit": "string",
          "customAttributes": {},
          "images": [
            0
          ],
          "relatedProducts": [
            0
          ],
          "crossSells": [
            0
          ],
          "upSells": [
            0
          ],
          "tags": [
            "string"
          ],
          "features": [
            "string"
          ],
          "itemPromotions": [
            0
          ],
          "productBundlePromotions": [
            0
          ],
          "directRestrictions": [
            "string"
          ],
          "userSegmentationBlacklist": [
            "string"
          ],
          "userSegmentationWhitelist": [
            "string"
          ],
          "primaryCategory": 0,
          "backorderable": true,
          "removeWhenOutOfStock": true,
          "taxCode": "string",
          "lastSyncDate": 0,
          "createdDate": 0,
          "lastModifiedDate": 0
        },
        "productId": "string",
        "promotions": "string",
        "bundleDiscounts": "string",
        "quantity": 0,
        "message": "string",
        "unitPrice": 0,
        "subTotal": 0,
        "subTotalBeforeDiscount": 0,
        "productTitle": "string",
        "productCategories": [
          0
        ],
        "addedFromCategoryId": 0,
        "addedFromCategoryName": "string",
        "productUrl": "string",
        "discount": 0,
        "itemDetails": {
          "fieldDisplayName": "string",
          "valueDisplayName": "string"
        },
        "backordered": true,
        "configured": true,
        "collectionId": "string",
        "subCollectionId": "string",
        "customText": "string",
        "thumbnailUrl": "string",
        "configurationSummaries": [
          "string"
        ],
        "customAttributes": {},
        "configurations": {},
        "orderItemFulfillments": {
          "fulfillmentProvider": "string",
          "fulfillmentProviderItemId": "string",
          "status": "string",
          "quantity": 0,
          "exportedToFulfillment": 0,
          "externalOrderId": "string",
          "shipOptionId": "string",
          "shipOptionName": "string",
          "shipOptionType": "string",
          "shipOptionCarrierName": "string",
          "shipOptionCarrierCode": "string",
          "shipOptionServiceCode": "string",
          "shipOptionDescription": "string",
          "shipOptionCustomCode": "string",
          "shipOptionCost": 0
        }
      }
    ],
    "billingAddress": {
      "id": 0,
      "gid": "string",
      "extId": "string",
      "label": "string",
      "title": "string",
      "suffix": "string",
      "firstName": "string",
      "middleName": "string",
      "lastName": "string",
      "careOf": "string",
      "address1": "string",
      "address2": "string",
      "address3": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string",
      "country": "string",
      "phone": "string",
      "email": "string",
      "poBox": true,
      "residential": true,
      "defaultShipping": true,
      "defaultBilling": true
    },
    "shippingAddress": {
      "id": 0,
      "gid": "string",
      "extId": "string",
      "label": "string",
      "title": "string",
      "suffix": "string",
      "firstName": "string",
      "middleName": "string",
      "lastName": "string",
      "careOf": "string",
      "address1": "string",
      "address2": "string",
      "address3": "string",
      "city": "string",
      "state": "string",
      "postalCode": "string",
      "country": "string",
      "phone": "string",
      "email": "string",
      "poBox": true,
      "residential": true,
      "defaultShipping": true,
      "defaultBilling": true
    },
    "billingAddressSameAsShipping": true,
    "email": "string",
    "fullName": "string",
    "specialInstructions": "string",
    "promotions": [
      {
        "id": 0,
        "title": "string",
        "description": "string",
        "message": "string",
        "active": true,
        "exclusive": true,
        "maximumDiscount": 0,
        "codes": [
          "string"
        ],
        "discountValueType": "string",
        "percent": 0,
        "amount": 0,
        "fixedCost": 0,
        "effectiveDiscount": 0
      }
    ],
    "shippingPromotions": [
      {
        "id": 0,
        "title": "string",
        "description": "string",
        "message": "string",
        "active": true,
        "exclusive": true,
        "maximumDiscount": 0,
        "codes": [
          "string"
        ],
        "discountValueType": "string",
        "percent": 0,
        "amount": 0,
        "fixedCost": 0,
        "effectiveDiscount": 0
      }
    ],
    "customer": 0,
    "giftMessage": "string",
    "baseShippingCost": 0,
    "finalShippingCost": 0,
    "totalCartLevelDiscount": 0,
    "totalShipLevelDiscount": 0,
    "totalTaxAmount": 0,
    "totalGiftCardAmount": 0,
    "subTotalOfItemsBeforeDiscounts": 0,
    "subTotalOfItemsAfterDiscounts": 0,
    "subTotalOfItemsAndShippingBeforeDiscounts": 0,
    "subTotalOfItemsAndShippingAfterDiscounts": 0,
    "subTotalOfItemsAndShippingAndTaxes": 0,
    "total": 0,
    "totalAfterAlternatePayments": 0,
    "status": "string",
    "currency": "string",
    "customerPoNumber": "string",
    "couponCodes": [
      "string"
    ],
    "shippingPoNumber": "string",
    "shippingCareOf": "string",
    "confirmationViewed": true,
    "customerIp": "string",
    "staffNotes": "string",
    "customerNotes": "string",
    "shipComplete": true,
    "shipAndBackorder": true,
    "giftCardUsage": {},
    "source": "string",
    "device": "string",
    "transactionId": "string",
    "paymentHandler": "string",
    "paymentInstrument": "string",
    "paymentInstrumentId": "string",
    "paymentStatus": "string",
    "paymentNotes": "string",
    "paymentSummary": "string",
    "paymentCaptureAmount": 0,
    "paymentCaptureDate": 0,
    "customAttributes": {},
    "createdDate": 0,
    "lastModifiedDate": 0
  }
]
```

<h3 id="get-orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|

<h3 id="get-orders-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[Order](#schemaorder)]|false|none|none|
|» id|integer(int64)|false|none|none|
|» guid|string|false|none|none|
|» extCartId|string|false|none|External cart ID based of which the order was created (if applicable).|
|» extSiteName|string|false|none|none|
|» extSiteOrderId|string|false|none|none|
|» extIntermediaryOrderId|string|false|none|none|
|» orderItems|[[OrderItem](#schemaorderitem)]|false|none|none|
|»» uuid|string|false|none|none|
|»» sku|[Sku](#schemasku)|false|none|none|
|»»» id|integer(int64)|false|read-only|none|
|»»» itemId|string|false|none|Unique SKU item ID|
|»»» productId|string|false|none|none|
|»»» slug|string|false|none|Unique, human-friendly identifier that is used in URLs.|
|»»» title|string|false|none|none|
|»»» description|string|false|none|none|
|»»» collection|string|false|none|none|
|»»» type|string|false|none|none|
|»»» subType|string|false|none|none|
|»»» status|string|false|none|none|
|»»» arrivalDate|integer(int64)|false|none|none|
|»»» eta|integer(int64)|false|none|none|
|»»» popularityIndex|integer|false|none|none|
|»»» online = true|boolean|false|none|none|
|»»» discontinued|boolean|false|none|none|
|»»» gender|string|false|none|none|
|»»» metaTitle|string|false|none|none|
|»»» metaDescription|string|false|none|none|
|»»» metaKeywords|string|false|none|none|
|»»» brandName|string|false|none|none|
|»»» seller|string|false|none|none|
|»»» manufacturerCode|string|false|none|none|
|»»» manufacturerName|string|false|none|none|
|»»» madeInCountry|string|false|none|none|
|»»» upc|string|false|none|none|
|»»» costPrice|number|false|none|none|
|»»» basePrice|number|false|none|none|
|»»» adjustedPrice|number|false|none|none|
|»»» salePrice|number|false|none|none|
|»»» currencyCode|string|false|none|none|
|»»» quantityAvailable|integer|false|none|none|
|»»» quantityIncrement|integer|false|none|none|
|»»» uom|string|false|none|none|
|»»» weight|integer|false|none|none|
|»»» weightUnit|string|false|none|none|
|»»» width|integer|false|none|none|
|»»» widthUnit|string|false|none|none|
|»»» length|integer|false|none|none|
|»»» lengthUnit|string|false|none|none|
|»»» height|integer|false|none|none|
|»»» heightUnit|string|false|none|none|
|»»» depth|integer|false|none|none|
|»»» depthUnit|string|false|none|none|
|»»» volume|integer|false|none|none|
|»»» volumeUnit|string|false|none|none|
|»»» customAttributes|object|false|none|none|
|»»» images|[integer]|false|none|none|
|»»» relatedProducts|[integer]|false|none|none|
|»»» crossSells|[integer]|false|none|none|
|»»» upSells|[integer]|false|none|none|
|»»» tags|[string]|false|none|none|
|»»» features|[string]|false|none|none|
|»»» itemPromotions|[integer]|false|none|none|
|»»» productBundlePromotions|[integer]|false|none|none|
|»»» directRestrictions|[string]|false|none|none|
|»»» userSegmentationBlacklist|[string]|false|none|none|
|»»» userSegmentationWhitelist|[string]|false|none|none|
|»»» primaryCategory|integer(int64)|false|none|none|
|»»» backorderable|boolean|false|none|none|
|»»» removeWhenOutOfStock|boolean|false|none|none|
|»»» taxCode|string|false|none|none|
|»»» lastSyncDate|integer(int64)|false|none|none|
|»»» createdDate|integer(int64)|false|read-only|none|
|»»» lastModifiedDate|integer(int64)|false|read-only|none|
|»» productId|string|false|none|none|
|»» promotions|string|false|none|none|
|»» bundleDiscounts|string|false|none|none|
|»» quantity|integer|false|none|none|
|»» message|string|false|none|none|
|»» unitPrice|number(double)|false|none|none|
|»» subTotal|number(double)|false|none|none|
|»» subTotalBeforeDiscount|number(double)|false|none|none|
|»» productTitle|string|false|none|none|
|»» productCategories|[integer]|false|none|none|
|»» addedFromCategoryId|integer(int64)|false|none|none|
|»» addedFromCategoryName|string|false|none|none|
|»» productUrl|string|false|none|none|
|»» discount|number(double)|false|none|none|
|»» itemDetails|object|false|none|none|
|»»» fieldDisplayName|string|false|none|none|
|»»» valueDisplayName|string|false|none|none|
|»» backordered|boolean|false|none|none|
|»» configured|boolean|false|none|none|
|»» collectionId|string|false|none|none|
|»» subCollectionId|string|false|none|none|
|»» customText|string|false|none|none|
|»» thumbnailUrl|string|false|none|none|
|»» configurationSummaries|[string]|false|none|none|
|»» customAttributes|object|false|none|none|
|»» configurations|object|false|none|none|
|»» orderItemFulfillments|[OrderItemFulfillment](#schemaorderitemfulfillment)|false|none|none|
|»»» fulfillmentProvider|string|false|none|none|
|»»» fulfillmentProviderItemId|string|false|none|none|
|»»» status|string|false|none|none|
|»»» quantity|integer|false|none|none|
|»»» exportedToFulfillment|number|false|none|none|
|»»» externalOrderId|string|false|none|none|
|»»» shipOptionId|string|false|none|none|
|»»» shipOptionName|string|false|none|none|
|»»» shipOptionType|string|false|none|none|
|»»» shipOptionCarrierName|string|false|none|none|
|»»» shipOptionCarrierCode|string|false|none|none|
|»»» shipOptionServiceCode|string|false|none|none|
|»»» shipOptionDescription|string|false|none|none|
|»»» shipOptionCustomCode|string|false|none|none|
|»»» shipOptionCost|number(double)|false|none|none|
|»» billingAddress|[Address](#schemaaddress)|false|none|none|
|»»» id|integer(int64)|false|read-only|none|
|»»» gid|string|false|none|none|
|»»» extId|string|false|none|none|
|»»» label|string|false|none|none|
|»»» title|string|false|none|none|
|»»» suffix|string|false|none|none|
|»»» firstName|string|false|none|none|
|»»» middleName|string|false|none|none|
|»»» lastName|string|false|none|none|
|»»» careOf|string|false|none|none|
|»»» address1|string|false|none|none|
|»»» address2|string|false|none|none|
|»»» address3|string|false|none|none|
|»»» city|string|false|none|none|
|»»» state|string|false|none|none|
|»»» postalCode|string|false|none|none|
|»»» country|string|false|none|none|
|»»» phone|string|false|none|none|
|»»» email|string|false|none|none|
|»»» poBox|boolean|false|none|none|
|»»» residential|boolean|false|none|none|
|»»» defaultShipping|boolean|false|none|none|
|»»» defaultBilling|boolean|false|none|none|
|»» shippingAddress|[Address](#schemaaddress)|false|none|none|
|»» billingAddressSameAsShipping|boolean|false|none|none|
|»» email|string|false|none|none|
|»» fullName|string|false|none|none|
|»» specialInstructions|string|false|none|none|
|»» promotions|[[Promotion](#schemapromotion)]|false|none|none|
|»»» id|integer(int64)|false|none|none|
|»»» title|string|false|none|none|
|»»» description|string|false|none|none|
|»»» message|string|false|none|none|
|»»» active|boolean|false|none|none|
|»»» exclusive|boolean|false|none|none|
|»»» maximumDiscount|number(double)|false|none|none|
|»»» codes|[string]|false|none|none|
|»»» discountValueType|string|false|none|none|
|»»» percent|number(double)|false|none|none|
|»»» amount|number(double)|false|none|none|
|»»» fixedCost|number(double)|false|none|none|
|»»» effectiveDiscount|number(double)|false|none|none|
|»» shippingPromotions|[[Promotion](#schemapromotion)]|false|none|none|
|»» customer|integer(int64)|false|none|none|
|»» giftMessage|string|false|none|none|
|»» baseShippingCost|number(double)|false|none|none|
|»» finalShippingCost|number(double)|false|none|none|
|»» totalCartLevelDiscount|number(double)|false|none|none|
|»» totalShipLevelDiscount|number(double)|false|none|none|
|»» totalTaxAmount|number(double)|false|none|none|
|»» totalGiftCardAmount|number(double)|false|none|none|
|»» subTotalOfItemsBeforeDiscounts|number(double)|false|none|none|
|»» subTotalOfItemsAfterDiscounts|number(double)|false|none|none|
|»» subTotalOfItemsAndShippingBeforeDiscounts|number(double)|false|none|none|
|»» subTotalOfItemsAndShippingAfterDiscounts|number(double)|false|none|none|
|»» subTotalOfItemsAndShippingAndTaxes|number(double)|false|none|none|
|»» total|number(double)|false|none|none|
|»» totalAfterAlternatePayments|number(double)|false|none|none|
|»» status|string|false|none|none|
|»» currency|string|false|none|none|
|»» customerPoNumber|string|false|none|none|
|»» couponCodes|[string]|false|none|none|
|»» shippingPoNumber|string|false|none|none|
|»» shippingCareOf|string|false|none|none|
|»» confirmationViewed|boolean|false|none|none|
|»» customerIp|string|false|none|none|
|»» staffNotes|string|false|none|none|
|»» customerNotes|string|false|none|none|
|»» shipComplete|boolean|false|none|none|
|»» shipAndBackorder|boolean|false|none|none|
|»» giftCardUsage|object|false|none|none|
|»» source|string|false|none|none|
|»» device|string|false|none|none|
|»» transactionId|string|false|none|none|
|»» paymentHandler|string|false|none|none|
|»» paymentInstrument|string|false|none|none|
|»» paymentInstrumentId|string|false|none|none|
|»» paymentStatus|string|false|none|none|
|»» paymentNotes|string|false|none|none|
|»» paymentSummary|string|false|none|none|
|»» paymentCaptureAmount|number(double)|false|none|none|
|»» paymentCaptureDate|integer(int64)|false|none|none|
|»» customAttributes|object|false|none|none|
|»» createdDate|integer(int64)|false|none|none|
|»» lastModifiedDate|integer(int64)|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

<h1 id="reactorone-api-fulfillments">Fulfillments</h1>

## Get Order Fulfillments

<a id="opIdGet Order Fulfillments"></a>

> Code samples

```http
GET https://dev-api.reactorone.net/api/2/orders/{orderId}/fulfillments HTTP/1.1
Host: dev-api.reactorone.net
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/orders/{orderId}/fulfillments',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/orders/{orderId}/fulfillments',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/orders/{orderId}/fulfillments");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`GET /orders/{orderId}/fulfillments`

*Retrieves fulfillments associated with an order*

<h3 id="get-order-fulfillments-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|orderId|path|integer(int64)|true|The order ID for which to retrieve fulfillments.|

> Example responses

> 200 Response

```json
{
  "orderId": 0,
  "orderGuid": "string",
  "extOrderId": "string",
  "extSiteOrderId": "string",
  "extSiteName": "string",
  "extIntermediaryOrderId": "string",
  "integrations": [
    "channeladvisor"
  ],
  "shipments": [
    {
      "fulfillmentProvider": "string",
      "trackingCode": "string",
      "shipCarrierCode": "FEDEX",
      "shipCarrierName": "string",
      "shipMethodCode": "FEDEX_GROUND",
      "shipMethodName": "string",
      "shipDate": 0,
      "fullOrderShipped": true,
      "items": [
        {
          "itemId": "string",
          "fulfillmentProviderItemId": "string",
          "quantityShipped": 0,
          "lineNo": 0
        }
      ]
    }
  ]
}
```

<h3 id="get-order-fulfillments-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|[OrderFulfillment](#schemaorderfulfillment)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

## Create Order Fulfillments

<a id="opIdCreate Order Fulfillments"></a>

> Code samples

```http
POST https://dev-api.reactorone.net/api/2/orders/fulfillments HTTP/1.1
Host: dev-api.reactorone.net
Content-Type: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json'

};

$.ajax({
  url: 'https://dev-api.reactorone.net/api/2/orders/fulfillments',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "fulfillments": [
    {
      "orderId": 0,
      "orderGuid": "string",
      "extOrderId": "string",
      "extSiteOrderId": "string",
      "extSiteName": "string",
      "extIntermediaryOrderId": "string",
      "integrations": [
        "channeladvisor"
      ],
      "shipments": [
        {
          "fulfillmentProvider": "string",
          "trackingCode": "string",
          "shipCarrierCode": "FEDEX",
          "shipCarrierName": "string",
          "shipMethodCode": "FEDEX_GROUND",
          "shipMethodName": "string",
          "shipDate": 0,
          "fullOrderShipped": true,
          "items": [
            {
              "itemId": "string",
              "fulfillmentProviderItemId": "string",
              "quantityShipped": 0,
              "lineNo": 0
            }
          ]
        }
      ]
    }
  ]
}';
const headers = {
  'Content-Type':'application/json'

};

fetch('https://dev-api.reactorone.net/api/2/orders/fulfillments',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```java
URL obj = new URL("https://dev-api.reactorone.net/api/2/orders/fulfillments");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

`POST /orders/fulfillments`

*Create new order fulfillments*

> Body parameter

```json
{
  "fulfillments": [
    {
      "orderId": 0,
      "orderGuid": "string",
      "extOrderId": "string",
      "extSiteOrderId": "string",
      "extSiteName": "string",
      "extIntermediaryOrderId": "string",
      "integrations": [
        "channeladvisor"
      ],
      "shipments": [
        {
          "fulfillmentProvider": "string",
          "trackingCode": "string",
          "shipCarrierCode": "FEDEX",
          "shipCarrierName": "string",
          "shipMethodCode": "FEDEX_GROUND",
          "shipMethodName": "string",
          "shipDate": 0,
          "fullOrderShipped": true,
          "items": [
            {
              "itemId": "string",
              "fulfillmentProviderItemId": "string",
              "quantityShipped": 0,
              "lineNo": 0
            }
          ]
        }
      ]
    }
  ]
}
```

<h3 id="create-order-fulfillments-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrderFulfillments](#schemaorderfulfillments)|false|none|

<h3 id="create-order-fulfillments-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None ( Scopes: admin )
</aside>

# Schemas

<h2 id="tocSanyvalue">AnyValue</h2>

<a id="schemaanyvalue"></a>

```json
"string"

```

### Properties

*anyOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

*or*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|number|false|none|none|

*or*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|integer|false|none|none|

*or*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|boolean|false|none|none|

*or*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[any]|false|none|none|

*or*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|

<h2 id="tocSaddress">Address</h2>

<a id="schemaaddress"></a>

```json
{
  "id": 0,
  "gid": "string",
  "extId": "string",
  "label": "string",
  "title": "string",
  "suffix": "string",
  "firstName": "string",
  "middleName": "string",
  "lastName": "string",
  "careOf": "string",
  "address1": "string",
  "address2": "string",
  "address3": "string",
  "city": "string",
  "state": "string",
  "postalCode": "string",
  "country": "string",
  "phone": "string",
  "email": "string",
  "poBox": true,
  "residential": true,
  "defaultShipping": true,
  "defaultBilling": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|gid|string|false|none|none|
|extId|string|false|none|none|
|label|string|false|none|none|
|title|string|false|none|none|
|suffix|string|false|none|none|
|firstName|string|false|none|none|
|middleName|string|false|none|none|
|lastName|string|false|none|none|
|careOf|string|false|none|none|
|address1|string|false|none|none|
|address2|string|false|none|none|
|address3|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postalCode|string|false|none|none|
|country|string|false|none|none|
|phone|string|false|none|none|
|email|string|false|none|none|
|poBox|boolean|false|none|none|
|residential|boolean|false|none|none|
|defaultShipping|boolean|false|none|none|
|defaultBilling|boolean|false|none|none|

<h2 id="tocSimage">Image</h2>

<a id="schemaimage"></a>

```json
{
  "id": 0,
  "gid": "string",
  "displayName": "string",
  "description": "string",
  "slug": "string",
  "tags": [
    "string"
  ],
  "filename": "string",
  "filePath": "string",
  "externalUrl": "string",
  "externalStorage": "string",
  "originalFilename": "string",
  "mediaType": "string",
  "extension": "string",
  "size": 0,
  "altText": "string",
  "md5Checksum": "string",
  "locale": "string",
  "url": "string",
  "type": "string",
  "view": "string",
  "width": 0,
  "height": 0,
  "quality": 0,
  "thumbnail": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|gid|string|false|none|none|
|displayName|string|false|none|none|
|description|string|false|none|none|
|slug|string|false|none|none|
|tags|[string]|false|none|none|
|filename|string|true|none|none|
|filePath|string|false|none|none|
|externalUrl|string|true|none|none|
|externalStorage|string|false|none|none|
|originalFilename|string|false|none|none|
|mediaType|string|false|none|none|
|extension|string|false|none|none|
|size|integer|false|none|Image file size in bytes|
|altText|string|false|none|none|
|md5Checksum|string|false|none|none|
|locale|string|false|none|none|
|url|string|false|none|none|
|type|string|false|none|none|
|view|string|false|none|none|
|width|integer|false|none|The image width in pixels|
|height|integer|false|none|The image height in pixels|
|quality|integer|false|none|The image quality (1-100)|
|thumbnail|string|false|none|none|

<h2 id="tocSorder">Order</h2>

<a id="schemaorder"></a>

```json
{
  "id": 0,
  "guid": "string",
  "extCartId": "string",
  "extSiteName": "string",
  "extSiteOrderId": "string",
  "extIntermediaryOrderId": "string",
  "orderItems": [
    {
      "uuid": "string",
      "sku": {
        "id": 0,
        "itemId": "string",
        "productId": "string",
        "slug": "string",
        "title": "string",
        "description": "string",
        "collection": "string",
        "type": "string",
        "subType": "string",
        "status": "string",
        "arrivalDate": 0,
        "eta": 0,
        "popularityIndex": 0,
        "online = true": true,
        "discontinued": true,
        "gender": "string",
        "metaTitle": "string",
        "metaDescription": "string",
        "metaKeywords": "string",
        "brandName": "string",
        "seller": "string",
        "manufacturerCode": "string",
        "manufacturerName": "string",
        "madeInCountry": "string",
        "upc": "string",
        "costPrice": 0,
        "basePrice": 0,
        "adjustedPrice": 0,
        "salePrice": 0,
        "currencyCode": "string",
        "quantityAvailable": 0,
        "quantityIncrement": 0,
        "uom": "string",
        "weight": 0,
        "weightUnit": "string",
        "width": 0,
        "widthUnit": "string",
        "length": 0,
        "lengthUnit": "string",
        "height": 0,
        "heightUnit": "string",
        "depth": 0,
        "depthUnit": "string",
        "volume": 0,
        "volumeUnit": "string",
        "customAttributes": {},
        "images": [
          0
        ],
        "relatedProducts": [
          0
        ],
        "crossSells": [
          0
        ],
        "upSells": [
          0
        ],
        "tags": [
          "string"
        ],
        "features": [
          "string"
        ],
        "itemPromotions": [
          0
        ],
        "productBundlePromotions": [
          0
        ],
        "directRestrictions": [
          "string"
        ],
        "userSegmentationBlacklist": [
          "string"
        ],
        "userSegmentationWhitelist": [
          "string"
        ],
        "primaryCategory": 0,
        "backorderable": true,
        "removeWhenOutOfStock": true,
        "taxCode": "string",
        "lastSyncDate": 0,
        "createdDate": 0,
        "lastModifiedDate": 0
      },
      "productId": "string",
      "promotions": "string",
      "bundleDiscounts": "string",
      "quantity": 0,
      "message": "string",
      "unitPrice": 0,
      "subTotal": 0,
      "subTotalBeforeDiscount": 0,
      "productTitle": "string",
      "productCategories": [
        0
      ],
      "addedFromCategoryId": 0,
      "addedFromCategoryName": "string",
      "productUrl": "string",
      "discount": 0,
      "itemDetails": {
        "fieldDisplayName": "string",
        "valueDisplayName": "string"
      },
      "backordered": true,
      "configured": true,
      "collectionId": "string",
      "subCollectionId": "string",
      "customText": "string",
      "thumbnailUrl": "string",
      "configurationSummaries": [
        "string"
      ],
      "customAttributes": {},
      "configurations": {},
      "orderItemFulfillments": {
        "fulfillmentProvider": "string",
        "fulfillmentProviderItemId": "string",
        "status": "string",
        "quantity": 0,
        "exportedToFulfillment": 0,
        "externalOrderId": "string",
        "shipOptionId": "string",
        "shipOptionName": "string",
        "shipOptionType": "string",
        "shipOptionCarrierName": "string",
        "shipOptionCarrierCode": "string",
        "shipOptionServiceCode": "string",
        "shipOptionDescription": "string",
        "shipOptionCustomCode": "string",
        "shipOptionCost": 0
      }
    }
  ],
  "billingAddress": {
    "id": 0,
    "gid": "string",
    "extId": "string",
    "label": "string",
    "title": "string",
    "suffix": "string",
    "firstName": "string",
    "middleName": "string",
    "lastName": "string",
    "careOf": "string",
    "address1": "string",
    "address2": "string",
    "address3": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "phone": "string",
    "email": "string",
    "poBox": true,
    "residential": true,
    "defaultShipping": true,
    "defaultBilling": true
  },
  "shippingAddress": {
    "id": 0,
    "gid": "string",
    "extId": "string",
    "label": "string",
    "title": "string",
    "suffix": "string",
    "firstName": "string",
    "middleName": "string",
    "lastName": "string",
    "careOf": "string",
    "address1": "string",
    "address2": "string",
    "address3": "string",
    "city": "string",
    "state": "string",
    "postalCode": "string",
    "country": "string",
    "phone": "string",
    "email": "string",
    "poBox": true,
    "residential": true,
    "defaultShipping": true,
    "defaultBilling": true
  },
  "billingAddressSameAsShipping": true,
  "email": "string",
  "fullName": "string",
  "specialInstructions": "string",
  "promotions": [
    {
      "id": 0,
      "title": "string",
      "description": "string",
      "message": "string",
      "active": true,
      "exclusive": true,
      "maximumDiscount": 0,
      "codes": [
        "string"
      ],
      "discountValueType": "string",
      "percent": 0,
      "amount": 0,
      "fixedCost": 0,
      "effectiveDiscount": 0
    }
  ],
  "shippingPromotions": [
    {
      "id": 0,
      "title": "string",
      "description": "string",
      "message": "string",
      "active": true,
      "exclusive": true,
      "maximumDiscount": 0,
      "codes": [
        "string"
      ],
      "discountValueType": "string",
      "percent": 0,
      "amount": 0,
      "fixedCost": 0,
      "effectiveDiscount": 0
    }
  ],
  "customer": 0,
  "giftMessage": "string",
  "baseShippingCost": 0,
  "finalShippingCost": 0,
  "totalCartLevelDiscount": 0,
  "totalShipLevelDiscount": 0,
  "totalTaxAmount": 0,
  "totalGiftCardAmount": 0,
  "subTotalOfItemsBeforeDiscounts": 0,
  "subTotalOfItemsAfterDiscounts": 0,
  "subTotalOfItemsAndShippingBeforeDiscounts": 0,
  "subTotalOfItemsAndShippingAfterDiscounts": 0,
  "subTotalOfItemsAndShippingAndTaxes": 0,
  "total": 0,
  "totalAfterAlternatePayments": 0,
  "status": "string",
  "currency": "string",
  "customerPoNumber": "string",
  "couponCodes": [
    "string"
  ],
  "shippingPoNumber": "string",
  "shippingCareOf": "string",
  "confirmationViewed": true,
  "customerIp": "string",
  "staffNotes": "string",
  "customerNotes": "string",
  "shipComplete": true,
  "shipAndBackorder": true,
  "giftCardUsage": {},
  "source": "string",
  "device": "string",
  "transactionId": "string",
  "paymentHandler": "string",
  "paymentInstrument": "string",
  "paymentInstrumentId": "string",
  "paymentStatus": "string",
  "paymentNotes": "string",
  "paymentSummary": "string",
  "paymentCaptureAmount": 0,
  "paymentCaptureDate": 0,
  "customAttributes": {},
  "createdDate": 0,
  "lastModifiedDate": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|guid|string|false|none|none|
|extCartId|string|false|none|External cart ID based of which the order was created (if applicable).|
|extSiteName|string|false|none|none|
|extSiteOrderId|string|false|none|none|
|extIntermediaryOrderId|string|false|none|none|
|orderItems|[[OrderItem](#schemaorderitem)]|false|none|none|
|billingAddress|[Address](#schemaaddress)|false|none|none|
|shippingAddress|[Address](#schemaaddress)|false|none|none|
|billingAddressSameAsShipping|boolean|false|none|none|
|email|string|false|none|none|
|fullName|string|false|none|none|
|specialInstructions|string|false|none|none|
|promotions|[[Promotion](#schemapromotion)]|false|none|none|
|shippingPromotions|[[Promotion](#schemapromotion)]|false|none|none|
|customer|integer(int64)|false|none|none|
|giftMessage|string|false|none|none|
|baseShippingCost|number(double)|false|none|none|
|finalShippingCost|number(double)|false|none|none|
|totalCartLevelDiscount|number(double)|false|none|none|
|totalShipLevelDiscount|number(double)|false|none|none|
|totalTaxAmount|number(double)|false|none|none|
|totalGiftCardAmount|number(double)|false|none|none|
|subTotalOfItemsBeforeDiscounts|number(double)|false|none|none|
|subTotalOfItemsAfterDiscounts|number(double)|false|none|none|
|subTotalOfItemsAndShippingBeforeDiscounts|number(double)|false|none|none|
|subTotalOfItemsAndShippingAfterDiscounts|number(double)|false|none|none|
|subTotalOfItemsAndShippingAndTaxes|number(double)|false|none|none|
|total|number(double)|false|none|none|
|totalAfterAlternatePayments|number(double)|false|none|none|
|status|string|false|none|none|
|currency|string|false|none|none|
|customerPoNumber|string|false|none|none|
|couponCodes|[string]|false|none|none|
|shippingPoNumber|string|false|none|none|
|shippingCareOf|string|false|none|none|
|confirmationViewed|boolean|false|none|none|
|customerIp|string|false|none|none|
|staffNotes|string|false|none|none|
|customerNotes|string|false|none|none|
|shipComplete|boolean|false|none|none|
|shipAndBackorder|boolean|false|none|none|
|giftCardUsage|object|false|none|none|
|source|string|false|none|none|
|device|string|false|none|none|
|transactionId|string|false|none|none|
|paymentHandler|string|false|none|none|
|paymentInstrument|string|false|none|none|
|paymentInstrumentId|string|false|none|none|
|paymentStatus|string|false|none|none|
|paymentNotes|string|false|none|none|
|paymentSummary|string|false|none|none|
|paymentCaptureAmount|number(double)|false|none|none|
|paymentCaptureDate|integer(int64)|false|none|none|
|customAttributes|object|false|none|none|
|createdDate|integer(int64)|false|none|none|
|lastModifiedDate|integer(int64)|false|none|none|

<h2 id="tocSorderfulfillments">OrderFulfillments</h2>

<a id="schemaorderfulfillments"></a>

```json
{
  "fulfillments": [
    {
      "orderId": 0,
      "orderGuid": "string",
      "extOrderId": "string",
      "extSiteOrderId": "string",
      "extSiteName": "string",
      "extIntermediaryOrderId": "string",
      "integrations": [
        "channeladvisor"
      ],
      "shipments": [
        {
          "fulfillmentProvider": "string",
          "trackingCode": "string",
          "shipCarrierCode": "FEDEX",
          "shipCarrierName": "string",
          "shipMethodCode": "FEDEX_GROUND",
          "shipMethodName": "string",
          "shipDate": 0,
          "fullOrderShipped": true,
          "items": [
            {
              "itemId": "string",
              "fulfillmentProviderItemId": "string",
              "quantityShipped": 0,
              "lineNo": 0
            }
          ]
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fulfillments|[[OrderFulfillment](#schemaorderfulfillment)]|false|none|[Must provide an order ID via one of the following properties: `orderId`, `orderGuid`, `extOrderId`, `extSiteOrderId`]|

<h2 id="tocSorderfulfillment">OrderFulfillment</h2>

<a id="schemaorderfulfillment"></a>

```json
{
  "orderId": 0,
  "orderGuid": "string",
  "extOrderId": "string",
  "extSiteOrderId": "string",
  "extSiteName": "string",
  "extIntermediaryOrderId": "string",
  "integrations": [
    "channeladvisor"
  ],
  "shipments": [
    {
      "fulfillmentProvider": "string",
      "trackingCode": "string",
      "shipCarrierCode": "FEDEX",
      "shipCarrierName": "string",
      "shipMethodCode": "FEDEX_GROUND",
      "shipMethodName": "string",
      "shipDate": 0,
      "fullOrderShipped": true,
      "items": [
        {
          "itemId": "string",
          "fulfillmentProviderItemId": "string",
          "quantityShipped": 0,
          "lineNo": 0
        }
      ]
    }
  ]
}

```

*Must provide an order ID via one of the following properties: `orderId`, `orderGuid`, `extOrderId`, `extSiteOrderId`*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|orderId|integer(int64)|false|none|none|
|orderGuid|string|false|none|none|
|extOrderId|string|false|none|none|
|extSiteOrderId|string|false|none|none|
|extSiteName|string|false|none|Only used when ReactorOne is used to sync order fulfillment status with external systems (e.g. Channel Advisor).|
|extIntermediaryOrderId|string|false|none|Only used when ReactorOne is used to sync order fulfillment status with external systems (e.g. Channel Advisor).|
|integrations|[string]|false|none|Indicates integrations that ReactorOne should send the updated order fulfillment status to.|
|shipments|[[OrderFulfillmentShipment](#schemaorderfulfillmentshipment)]|false|none|none|

<h2 id="tocSorderfulfillmentshipment">OrderFulfillmentShipment</h2>

<a id="schemaorderfulfillmentshipment"></a>

```json
{
  "fulfillmentProvider": "string",
  "trackingCode": "string",
  "shipCarrierCode": "FEDEX",
  "shipCarrierName": "string",
  "shipMethodCode": "FEDEX_GROUND",
  "shipMethodName": "string",
  "shipDate": 0,
  "fullOrderShipped": true,
  "items": [
    {
      "itemId": "string",
      "fulfillmentProviderItemId": "string",
      "quantityShipped": 0,
      "lineNo": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fulfillmentProvider|string|true|none|The ID of the fulfillment provider that is fulfilling the shipped items.|
|trackingCode|string|false|none|none|
|shipCarrierCode|string|false|none|none|
|shipCarrierName|string|false|none|none|
|shipMethodCode|string|false|none|none|
|shipMethodName|string|false|none|none|
|shipDate|integer(int64)|false|none|none|
|fullOrderShipped|boolean|false|none|If `true`, individual item info may be omitted.|
|items|[object]|false|none|none|
|» itemId|string|true|none|The SKU item ID.|
|» fulfillmentProviderItemId|string|false|none|The fulfillment provider SKU item ID if different than the primary SKU item ID.|
|» quantityShipped|integer|true|none|none|
|» lineNo|integer|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|shipCarrierCode|FEDEX|
|shipCarrierCode|UPS|
|shipCarrierCode|USPS|
|shipCarrierCode|DHL|
|shipCarrierCode|AIRBORNE|
|shipCarrierCode|FREIGHT|
|shipMethodCode|FEDEX_GROUND|
|shipMethodCode|FEDEX_GROUND_HOME|
|shipMethodCode|FEDEX_2DAY|
|shipMethodCode|FEDEX_PRIORITY|
|shipMethodCode|FEDEX_EXPSAVER|
|shipMethodCode|FEDEX_OVERNIGHT|
|shipMethodCode|FEDEX_1STOVERNIGHT|
|shipMethodCode|FEDEX_OVERNIGHT_FREIGHT|
|shipMethodCode|FEDEX_2DAY_FREIGHT|
|shipMethodCode|FEDEX_EXPSAVER_FREIGHT|
|shipMethodCode|FEDEX_INTL_PRIORITY|
|shipMethodCode|FEDEX_OVERNIGHT_INTL_ECONOMY|
|shipMethodCode|FEDEX_INTL_FIRST|
|shipMethodCode|FEDEX_INTL_ECONOMY|
|shipMethodCode|FEDEX_SMARTPOST|
|shipMethodCode|UPS_2DAA|
|shipMethodCode|UPS_2DAY|
|shipMethodCode|UPS_3DS|
|shipMethodCode|UPS_ES|
|shipMethodCode|UPS_GROUND|
|shipMethodCode|UPS_NDAEA|
|shipMethodCode|UPS_NEXTDAY|
|shipMethodCode|UPS_NDAS|
|shipMethodCode|UPS_STD|
|shipMethodCode|UPS_WWEX|
|shipMethodCode|UPS_WWE|
|shipMethodCode|UPS_WWEP|
|shipMethodCode|USPS_AMLP|
|shipMethodCode|USPS_APP|
|shipMethodCode|USPS_ESLP|
|shipMethodCode|USPS_GEM|
|shipMethodCode|USPS_FIRSTCLASS|
|shipMethodCode|USPS_GEGDS|
|shipMethodCode|USPS_GEGNDS|
|shipMethodCode|USPS_GPMFLEL|
|shipMethodCode|USPS_GPMDRES|
|shipMethodCode|USPS_GPMVWES|
|shipMethodCode|USPS_MEDIA|
|shipMethodCode|USPS_PARCELPOST|
|shipMethodCode|USPS_PRIORITY|
|shipMethodCode|USPS_EXPRESS|
|shipMethodCode|USPS_INTLPARCEL|
|shipMethodCode|USPS_POSTCARD|
|shipMethodCode|USPS_LIBRARYMAIL|
|shipMethodCode|USPS_BOUNDPRINTEDMATTER|
|shipMethodCode|USPS_PRESORTEDFIRST|
|shipMethodCode|USPS_PRESORTEDSTANDARD|
|shipMethodCode|USPS_INTLLETTER|
|shipMethodCode|USPS_INTLAIRLETTER|
|shipMethodCode|USPS_INTLPOSTCARD|
|shipMethodCode|USPS_INTLAEROGRAMME|
|shipMethodCode|USPS_INTLAIRPARCEL|
|shipMethodCode|USPS_IECONOMY|
|shipMethodCode|USPS_IFIRSTCLASS|
|shipMethodCode|USPS_IPRIORITY|
|shipMethodCode|DHL_STANDARD|
|shipMethodCode|AIRBORNE_GROUND|
|shipMethodCode|AIRBORNE_2DAY|
|shipMethodCode|AIRBORNE_OVERNIGHT|
|shipMethodCode|FREIGHT_GROUND|

<h2 id="tocSorderitem">OrderItem</h2>

<a id="schemaorderitem"></a>

```json
{
  "uuid": "string",
  "sku": {
    "id": 0,
    "itemId": "string",
    "productId": "string",
    "slug": "string",
    "title": "string",
    "description": "string",
    "collection": "string",
    "type": "string",
    "subType": "string",
    "status": "string",
    "arrivalDate": 0,
    "eta": 0,
    "popularityIndex": 0,
    "online = true": true,
    "discontinued": true,
    "gender": "string",
    "metaTitle": "string",
    "metaDescription": "string",
    "metaKeywords": "string",
    "brandName": "string",
    "seller": "string",
    "manufacturerCode": "string",
    "manufacturerName": "string",
    "madeInCountry": "string",
    "upc": "string",
    "costPrice": 0,
    "basePrice": 0,
    "adjustedPrice": 0,
    "salePrice": 0,
    "currencyCode": "string",
    "quantityAvailable": 0,
    "quantityIncrement": 0,
    "uom": "string",
    "weight": 0,
    "weightUnit": "string",
    "width": 0,
    "widthUnit": "string",
    "length": 0,
    "lengthUnit": "string",
    "height": 0,
    "heightUnit": "string",
    "depth": 0,
    "depthUnit": "string",
    "volume": 0,
    "volumeUnit": "string",
    "customAttributes": {},
    "images": [
      0
    ],
    "relatedProducts": [
      0
    ],
    "crossSells": [
      0
    ],
    "upSells": [
      0
    ],
    "tags": [
      "string"
    ],
    "features": [
      "string"
    ],
    "itemPromotions": [
      0
    ],
    "productBundlePromotions": [
      0
    ],
    "directRestrictions": [
      "string"
    ],
    "userSegmentationBlacklist": [
      "string"
    ],
    "userSegmentationWhitelist": [
      "string"
    ],
    "primaryCategory": 0,
    "backorderable": true,
    "removeWhenOutOfStock": true,
    "taxCode": "string",
    "lastSyncDate": 0,
    "createdDate": 0,
    "lastModifiedDate": 0
  },
  "productId": "string",
  "promotions": "string",
  "bundleDiscounts": "string",
  "quantity": 0,
  "message": "string",
  "unitPrice": 0,
  "subTotal": 0,
  "subTotalBeforeDiscount": 0,
  "productTitle": "string",
  "productCategories": [
    0
  ],
  "addedFromCategoryId": 0,
  "addedFromCategoryName": "string",
  "productUrl": "string",
  "discount": 0,
  "itemDetails": {
    "fieldDisplayName": "string",
    "valueDisplayName": "string"
  },
  "backordered": true,
  "configured": true,
  "collectionId": "string",
  "subCollectionId": "string",
  "customText": "string",
  "thumbnailUrl": "string",
  "configurationSummaries": [
    "string"
  ],
  "customAttributes": {},
  "configurations": {},
  "orderItemFulfillments": {
    "fulfillmentProvider": "string",
    "fulfillmentProviderItemId": "string",
    "status": "string",
    "quantity": 0,
    "exportedToFulfillment": 0,
    "externalOrderId": "string",
    "shipOptionId": "string",
    "shipOptionName": "string",
    "shipOptionType": "string",
    "shipOptionCarrierName": "string",
    "shipOptionCarrierCode": "string",
    "shipOptionServiceCode": "string",
    "shipOptionDescription": "string",
    "shipOptionCustomCode": "string",
    "shipOptionCost": 0
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|uuid|string|false|none|none|
|sku|[Sku](#schemasku)|false|none|none|
|productId|string|false|none|none|
|promotions|string|false|none|none|
|bundleDiscounts|string|false|none|none|
|quantity|integer|false|none|none|
|message|string|false|none|none|
|unitPrice|number(double)|false|none|none|
|subTotal|number(double)|false|none|none|
|subTotalBeforeDiscount|number(double)|false|none|none|
|productTitle|string|false|none|none|
|productCategories|[integer]|false|none|none|
|addedFromCategoryId|integer(int64)|false|none|none|
|addedFromCategoryName|string|false|none|none|
|productUrl|string|false|none|none|
|discount|number(double)|false|none|none|
|itemDetails|object|false|none|none|
|» fieldDisplayName|string|false|none|none|
|» valueDisplayName|string|false|none|none|
|backordered|boolean|false|none|none|
|configured|boolean|false|none|none|
|collectionId|string|false|none|none|
|subCollectionId|string|false|none|none|
|customText|string|false|none|none|
|thumbnailUrl|string|false|none|none|
|configurationSummaries|[string]|false|none|none|
|customAttributes|object|false|none|none|
|configurations|object|false|none|none|
|orderItemFulfillments|[OrderItemFulfillment](#schemaorderitemfulfillment)|false|none|none|

<h2 id="tocSorderitemfulfillment">OrderItemFulfillment</h2>

<a id="schemaorderitemfulfillment"></a>

```json
{
  "fulfillmentProvider": "string",
  "fulfillmentProviderItemId": "string",
  "status": "string",
  "quantity": 0,
  "exportedToFulfillment": 0,
  "externalOrderId": "string",
  "shipOptionId": "string",
  "shipOptionName": "string",
  "shipOptionType": "string",
  "shipOptionCarrierName": "string",
  "shipOptionCarrierCode": "string",
  "shipOptionServiceCode": "string",
  "shipOptionDescription": "string",
  "shipOptionCustomCode": "string",
  "shipOptionCost": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fulfillmentProvider|string|false|none|none|
|fulfillmentProviderItemId|string|false|none|none|
|status|string|false|none|none|
|quantity|integer|false|none|none|
|exportedToFulfillment|number|false|none|none|
|externalOrderId|string|false|none|none|
|shipOptionId|string|false|none|none|
|shipOptionName|string|false|none|none|
|shipOptionType|string|false|none|none|
|shipOptionCarrierName|string|false|none|none|
|shipOptionCarrierCode|string|false|none|none|
|shipOptionServiceCode|string|false|none|none|
|shipOptionDescription|string|false|none|none|
|shipOptionCustomCode|string|false|none|none|
|shipOptionCost|number(double)|false|none|none|

<h2 id="tocSproduct">Product</h2>

<a id="schemaproduct"></a>

```json
{
  "itemId": "string",
  "slug": "string",
  "title": "string",
  "description": "string",
  "summary": "string",
  "online": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "masterSku": "string",
  "skus": [
    {
      "id": 0,
      "itemId": "string",
      "productId": "string",
      "slug": "string",
      "title": "string",
      "description": "string",
      "collection": "string",
      "type": "string",
      "subType": "string",
      "status": "string",
      "arrivalDate": 0,
      "eta": 0,
      "popularityIndex": 0,
      "online = true": true,
      "discontinued": true,
      "gender": "string",
      "metaTitle": "string",
      "metaDescription": "string",
      "metaKeywords": "string",
      "brandName": "string",
      "seller": "string",
      "manufacturerCode": "string",
      "manufacturerName": "string",
      "madeInCountry": "string",
      "upc": "string",
      "costPrice": 0,
      "basePrice": 0,
      "adjustedPrice": 0,
      "salePrice": 0,
      "currencyCode": "string",
      "quantityAvailable": 0,
      "quantityIncrement": 0,
      "uom": "string",
      "weight": 0,
      "weightUnit": "string",
      "width": 0,
      "widthUnit": "string",
      "length": 0,
      "lengthUnit": "string",
      "height": 0,
      "heightUnit": "string",
      "depth": 0,
      "depthUnit": "string",
      "volume": 0,
      "volumeUnit": "string",
      "customAttributes": {},
      "images": [
        0
      ],
      "relatedProducts": [
        0
      ],
      "crossSells": [
        0
      ],
      "upSells": [
        0
      ],
      "tags": [
        "string"
      ],
      "features": [
        "string"
      ],
      "itemPromotions": [
        0
      ],
      "productBundlePromotions": [
        0
      ],
      "directRestrictions": [
        "string"
      ],
      "userSegmentationBlacklist": [
        "string"
      ],
      "userSegmentationWhitelist": [
        "string"
      ],
      "primaryCategory": 0,
      "backorderable": true,
      "removeWhenOutOfStock": true,
      "taxCode": "string",
      "lastSyncDate": 0,
      "createdDate": 0,
      "lastModifiedDate": 0
    }
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "variationAttributes": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "customProductAttributes": {},
  "searchKeywords": [
    {
      "input": "string",
      "weight": 0
    }
  ],
  "createdDate": 0,
  "lastModifiedDate": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|true|none|Unique product ID.|
|slug|string|false|none|Unique, human-friendly product identifier that is used in URLs. Generated from master SKU if not provided.|
|title|string|false|none|The product title. Uses master SKU title if not provided.|
|description|string|false|none|The product description (supports HTML). Uses master SKU description if not provided.|
|summary|string|false|none|The product summary (supports HTML).|
|online|boolean|false|none|Indicates whether the product is online. Defaults to `true`.|
|metaTitle|string|false|none|The title of the product used for SEO purposes. Generally added to the `<meta name='title'>` tag. Uses `title` if not provided.|
|metaDescription|string|false|none|The description of the product used for SEO purposes. Generally added to the `<meta name='description'>` tag Uses `description` if not provided|
|metaKeywords|string|false|none|The keywords of the product used for SEO purposes. Generally added to the `<meta name='keywords'>` tag.|
|masterSku|string|false|none|The `itemId` of the master/primary SKU.|
|skus|[[Sku](#schemasku)]|false|none|New or existing SKUs associated with the product.|
|images|[[Image](#schemaimage)]|false|none|New or existing images associated with the product.|
|variationAttributes|[string]|false|none|Variation attributes to be used for the product (e.g. `color`, `size`).|
|tags|[string]|false|none|none|
|customProductAttributes|object|false|none|Custom product attributes provided as key-value pairs. Both keys and values must be strings.|
|searchKeywords|[[SearchKeyword](#schemasearchkeyword)]|false|none|Search keywords to be used in the product search.|
|createdDate|integer(int64)|false|read-only|none|
|lastModifiedDate|integer(int64)|false|read-only|none|

<h2 id="tocSpromotion">Promotion</h2>

<a id="schemapromotion"></a>

```json
{
  "id": 0,
  "title": "string",
  "description": "string",
  "message": "string",
  "active": true,
  "exclusive": true,
  "maximumDiscount": 0,
  "codes": [
    "string"
  ],
  "discountValueType": "string",
  "percent": 0,
  "amount": 0,
  "fixedCost": 0,
  "effectiveDiscount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|title|string|false|none|none|
|description|string|false|none|none|
|message|string|false|none|none|
|active|boolean|false|none|none|
|exclusive|boolean|false|none|none|
|maximumDiscount|number(double)|false|none|none|
|codes|[string]|false|none|none|
|discountValueType|string|false|none|none|
|percent|number(double)|false|none|none|
|amount|number(double)|false|none|none|
|fixedCost|number(double)|false|none|none|
|effectiveDiscount|number(double)|false|none|none|

<h2 id="tocSreportrequest">ReportRequest</h2>

<a id="schemareportrequest"></a>

```json
{
  "startDate": "2019-04-25T19:59:37Z",
  "endDate": "2019-04-25T19:59:37Z",
  "metrics": [
    {
      "name": "string",
      "dimensions": [
        "string"
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|startDate|string(date-time)|false|none|Start date in ISO 8601 format (e.g. 2017-07-21T17:32:28Z). Other valid values: `today`|
|endDate|string(date-time)|false|none|End date in ISO 8601 format (e.g. 2017-07-21T17:32:28Z). Other valid values: `today`|
|metrics|[object]|false|none|none|
|» name|string|false|none|none|
|» dimensions|[string]|false|none|none|

<h2 id="tocSreportresponse">ReportResponse</h2>

<a id="schemareportresponse"></a>

```json
{
  "startDate": "string",
  "endDate": "string",
  "metrics": [
    {
      "name": "string",
      "dimensions": [
        {
          "name": "string",
          "value": "string"
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|startDate|string|true|none|none|
|endDate|string|true|none|none|
|metrics|[object]|false|none|none|
|» name|string|false|none|none|
|» dimensions|[object]|false|none|none|
|»» name|string|false|none|none|
|»» value|[AnyValue](#schemaanyvalue)|false|none|none|

<h2 id="tocSsearchkeyword">SearchKeyword</h2>

<a id="schemasearchkeyword"></a>

```json
{
  "input": "string",
  "weight": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|input|string|false|none|The search keyword.|
|weight|integer|false|none|The search weight of the keyword.|

<h2 id="tocSsku">Sku</h2>

<a id="schemasku"></a>

```json
{
  "id": 0,
  "itemId": "string",
  "productId": "string",
  "slug": "string",
  "title": "string",
  "description": "string",
  "collection": "string",
  "type": "string",
  "subType": "string",
  "status": "string",
  "arrivalDate": 0,
  "eta": 0,
  "popularityIndex": 0,
  "online = true": true,
  "discontinued": true,
  "gender": "string",
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "brandName": "string",
  "seller": "string",
  "manufacturerCode": "string",
  "manufacturerName": "string",
  "madeInCountry": "string",
  "upc": "string",
  "costPrice": 0,
  "basePrice": 0,
  "adjustedPrice": 0,
  "salePrice": 0,
  "currencyCode": "string",
  "quantityAvailable": 0,
  "quantityIncrement": 0,
  "uom": "string",
  "weight": 0,
  "weightUnit": "string",
  "width": 0,
  "widthUnit": "string",
  "length": 0,
  "lengthUnit": "string",
  "height": 0,
  "heightUnit": "string",
  "depth": 0,
  "depthUnit": "string",
  "volume": 0,
  "volumeUnit": "string",
  "customAttributes": {},
  "images": [
    0
  ],
  "relatedProducts": [
    0
  ],
  "crossSells": [
    0
  ],
  "upSells": [
    0
  ],
  "tags": [
    "string"
  ],
  "features": [
    "string"
  ],
  "itemPromotions": [
    0
  ],
  "productBundlePromotions": [
    0
  ],
  "directRestrictions": [
    "string"
  ],
  "userSegmentationBlacklist": [
    "string"
  ],
  "userSegmentationWhitelist": [
    "string"
  ],
  "primaryCategory": 0,
  "backorderable": true,
  "removeWhenOutOfStock": true,
  "taxCode": "string",
  "lastSyncDate": 0,
  "createdDate": 0,
  "lastModifiedDate": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|read-only|none|
|itemId|string|false|none|Unique SKU item ID|
|productId|string|false|none|none|
|slug|string|false|none|Unique, human-friendly identifier that is used in URLs.|
|title|string|false|none|none|
|description|string|false|none|none|
|collection|string|false|none|none|
|type|string|false|none|none|
|subType|string|false|none|none|
|status|string|false|none|none|
|arrivalDate|integer(int64)|false|none|none|
|eta|integer(int64)|false|none|none|
|popularityIndex|integer|false|none|none|
|online = true|boolean|false|none|none|
|discontinued|boolean|false|none|none|
|gender|string|false|none|none|
|metaTitle|string|false|none|none|
|metaDescription|string|false|none|none|
|metaKeywords|string|false|none|none|
|brandName|string|false|none|none|
|seller|string|false|none|none|
|manufacturerCode|string|false|none|none|
|manufacturerName|string|false|none|none|
|madeInCountry|string|false|none|none|
|upc|string|false|none|none|
|costPrice|number|false|none|none|
|basePrice|number|false|none|none|
|adjustedPrice|number|false|none|none|
|salePrice|number|false|none|none|
|currencyCode|string|false|none|none|
|quantityAvailable|integer|false|none|none|
|quantityIncrement|integer|false|none|none|
|uom|string|false|none|none|
|weight|integer|false|none|none|
|weightUnit|string|false|none|none|
|width|integer|false|none|none|
|widthUnit|string|false|none|none|
|length|integer|false|none|none|
|lengthUnit|string|false|none|none|
|height|integer|false|none|none|
|heightUnit|string|false|none|none|
|depth|integer|false|none|none|
|depthUnit|string|false|none|none|
|volume|integer|false|none|none|
|volumeUnit|string|false|none|none|
|customAttributes|object|false|none|none|
|images|[integer]|false|none|none|
|relatedProducts|[integer]|false|none|none|
|crossSells|[integer]|false|none|none|
|upSells|[integer]|false|none|none|
|tags|[string]|false|none|none|
|features|[string]|false|none|none|
|itemPromotions|[integer]|false|none|none|
|productBundlePromotions|[integer]|false|none|none|
|directRestrictions|[string]|false|none|none|
|userSegmentationBlacklist|[string]|false|none|none|
|userSegmentationWhitelist|[string]|false|none|none|
|primaryCategory|integer(int64)|false|none|none|
|backorderable|boolean|false|none|none|
|removeWhenOutOfStock|boolean|false|none|none|
|taxCode|string|false|none|none|
|lastSyncDate|integer(int64)|false|none|none|
|createdDate|integer(int64)|false|read-only|none|
|lastModifiedDate|integer(int64)|false|read-only|none|

<h2 id="tocSskufulfillmentprovider">SkuFulfillmentProvider</h2>

<a id="schemaskufulfillmentprovider"></a>

```json
{
  "id": "string",
  "sku": {
    "itemId": "string",
    "quantityAvailable": 0,
    "online": true,
    "discontinued": true,
    "backorderable": true
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|true|none|none|
|sku|object|false|none|Optional fulfillment provider specific SKU data in case they differ from the main SKU data.|
|» itemId|string|false|none|The unique fulfillment provider specific SKU item ID.|
|» quantityAvailable|integer|false|none|The quantity available from the fulfillment provider.|
|» online|boolean|false|none|Whether the SKU is online or not.|
|» discontinued|boolean|false|none|Whether the SKU is discontinued or not.|
|» backorderable|boolean|false|none|Whether the SKU can be backordered.|

<h2 id="tocSskuimport">SkuImport</h2>

<a id="schemaskuimport"></a>

```json
{
  "itemId": "string",
  "productId": "string",
  "title": "string",
  "slug": "string",
  "description": "string",
  "summary": "string",
  "collection": "string",
  "type": "string",
  "subType": "string",
  "status": "string",
  "popularityIndex": 0,
  "online": true,
  "discontinued": true,
  "metaTitle": "string",
  "metaDescription": "string",
  "metaKeywords": "string",
  "brandName": "string",
  "seller": "string",
  "manufacturerCode": "string",
  "manufacturerName": "string",
  "madeInCountry": "string",
  "upc": "string",
  "currencyCode": "string",
  "quantityAvailable": 0,
  "quantityIncrement": 0,
  "uom": "string",
  "weight": 0,
  "weightUnit": "string",
  "width": 0,
  "widthUnit": "string",
  "length": 0,
  "lengthUnit": "string",
  "height": 0,
  "heightUnit": "string",
  "depth": 0,
  "depthUnit": "string",
  "volume": 0,
  "volumeUnit": "string",
  "backorderable": true,
  "removeWhenOutOfStock": true,
  "costPrice": 0,
  "basePrice": 0,
  "adjustedPrice": 0,
  "salePrice": 0,
  "arrivalDate": 0,
  "eta": 0,
  "gender": "string",
  "taxCode": "string",
  "customAttributes": {},
  "features": [
    "string"
  ],
  "tags": [
    "string"
  ],
  "images": [
    {
      "id": 0,
      "gid": "string",
      "displayName": "string",
      "description": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "filename": "string",
      "filePath": "string",
      "externalUrl": "string",
      "externalStorage": "string",
      "originalFilename": "string",
      "mediaType": "string",
      "extension": "string",
      "size": 0,
      "altText": "string",
      "md5Checksum": "string",
      "locale": "string",
      "url": "string",
      "type": "string",
      "view": "string",
      "width": 0,
      "height": 0,
      "quality": 0,
      "thumbnail": "string"
    }
  ],
  "fulfillmentProviders": [
    {
      "id": "string",
      "sku": {
        "itemId": "string",
        "quantityAvailable": 0,
        "online": true,
        "discontinued": true,
        "backorderable": true
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|itemId|string|true|none|Unique SKU item ID|
|productId|string|true|none|Product ID used to group multiple SKUs|
|title|string|true|none|none|
|slug|string|false|none|none|
|description|string|false|none|none|
|summary|string|false|none|none|
|collection|string|false|none|none|
|type|string|false|none|none|
|subType|string|false|none|none|
|status|string|false|none|none|
|popularityIndex|integer|false|none|none|
|online|boolean|false|none|none|
|discontinued|boolean|false|none|none|
|metaTitle|string|false|none|none|
|metaDescription|string|false|none|none|
|metaKeywords|string|false|none|none|
|brandName|string|false|none|none|
|seller|string|false|none|none|
|manufacturerCode|string|false|none|none|
|manufacturerName|string|false|none|none|
|madeInCountry|string|false|none|none|
|upc|string|false|none|none|
|currencyCode|string|false|none|none|
|quantityAvailable|integer|false|none|none|
|quantityIncrement|integer|false|none|none|
|uom|string|false|none|none|
|weight|number|false|none|none|
|weightUnit|string|false|none|none|
|width|number|false|none|none|
|widthUnit|string|false|none|none|
|length|number|false|none|none|
|lengthUnit|string|false|none|none|
|height|number|false|none|none|
|heightUnit|string|false|none|none|
|depth|number|false|none|none|
|depthUnit|string|false|none|none|
|volume|number|false|none|none|
|volumeUnit|string|false|none|none|
|backorderable|boolean|false|none|none|
|removeWhenOutOfStock|boolean|false|none|none|
|costPrice|number|false|none|none|
|basePrice|number|false|none|none|
|adjustedPrice|number|false|none|none|
|salePrice|number|false|none|none|
|arrivalDate|number|false|none|none|
|eta|number|false|none|none|
|gender|string|false|none|none|
|taxCode|string|false|none|none|
|customAttributes|object|false|none|none|
|features|[string]|false|none|none|
|tags|[string]|false|none|none|
|images|[[Image](#schemaimage)]|false|none|none|
|fulfillmentProviders|[[SkuFulfillmentProvider](#schemaskufulfillmentprovider)]|false|none|none|

