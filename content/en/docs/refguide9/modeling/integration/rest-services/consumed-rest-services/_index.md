---
title: "Consumed REST Services"
url: /refguide9/consumed-rest-services/
description: "Presents an overview of consumed REST services and JSON in Mendix."
weight: 15
tags: ["studio pro"]
#If moving or renaming this doc file, implement a temporary redirect and let the respective team know they should update the URL in the product. See Mapping to Products for more details.
---

## 1 REST {#rest}

Representational state transfer (REST) is an approach to consuming or exposing resources. It has gained popularity because of its simplicity, because no extensive schemas or contracts are needed to transfer data between endpoints. It uses the following:

* HTTP URLs to locate resources
* HTTP headers to authenticate and specify [content types](#content-types) (such as XML or JSON)
* HTTP methods to identify operations on resources, such as GET (retrieve data) or POST (send data)

Lack of contracts and schemas give you an easy start to using REST. However, many REST endpoints return complex data.

The [JSON Structure](/refguide9/json-structures/) document helps with giving structure to JSON data: from an example JSON snippet, a lightweight schema is extracted that is used in [Mapping Documents](/refguide9/mapping-documents/). The [Import Mapping](/refguide9/import-mappings/) document converts JSON (or XML) to Mendix objects, and the [Export Mapping](/refguide9/export-mappings/) document serializes Mendix objects to JSON (or XML).

### 1.1 Content Types {#content-types}

Content types are included in [custom HTTP headers](/refguide9/call-rest-action/#custom-http-headers) to specify the output of the call, including media type or data format. For more information on content types, see [Content Negotiation in REST](https://restfulapi.net/content-negotiation/).

## 2 JSON

JavaScript object notation (JSON) is a lightweight representation of data. 

```js
{
	"name": "John Smith",
	"age": 23,
	"address": 
	{
		"street": "Dopeylane 14",
		"city": "Worchestire"
	}
}
```

Above, the object `person` is described with the corresponding values for the attributes `name`, `age`, and the referred object `address`.

REST calls that output JSON need to declare the [content type](#content-types) as `application/JSON`. 
