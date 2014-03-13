## Order
Order reprezentuje objednávku zákazníka. Obsahuje více požadavků (Request)

### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of order</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>requests</strong></td>
    <td><em>array</em></td>
    <td>Pole požadavků (Request)</td>
    <td><code>{"object_type":"contact","handle":"KUBICEK","request_type":"register"}</code></td>
  </tr>
  <tr>
    <td><strong>external_id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor objednávky v systému zákazníka</td>
    <td><code>"our_customer_invoice_35"</code></td>
  </tr>
</table>

### Order Create
Podání nové objednávky.

```
POST /orders
```

#### Required Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>requests</strong></td>
    <td><em>array</em></td>
    <td>Pole požadavků (Request)</td>
    <td><code>{"object_type":"contact","handle":"KUBICEK","request_type":"register"}</code></td>
  </tr>
</table>


#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of order</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>external_id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor objednávky v systému zákazníka</td>
    <td><code>"our_customer_invoice_35"</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST /orders \
-H "Content-Type: application/json" \
-d '{"id":null,"requests":null,"external_id":null}'
```

#### Response Example
```
HTTP/1.1 201 Created
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "requests": {
    "object_type": "contact",
    "handle": "KUBICEK",
    "request_type": "register"
  },
  "external_id": "our_customer_invoice_35"
}
```

### Order Info
Informace o konkrétní objednávce.

```
GET /orders/{order_id}
```


#### Curl Example
```term
$ curl -n -X GET /orders/$order_id
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "requests": {
    "object_type": "contact",
    "handle": "KUBICEK",
    "request_type": "register"
  },
  "external_id": "our_customer_invoice_35"
}
```

### Order List
Seznam objednávek.

```
GET /orders
```


#### Curl Example
```term
$ curl -n -X GET /orders
```

#### Response Example
```
HTTP/1.1 200 OK
Accept-Range: id
Content-Range: id 01234567-89ab-cdef-0123-456789abcdef..01234567-89ab-cdef-0123-456789abcdef; max=200
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
[
  {
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "requests": {
      "object_type": "contact",
      "handle": "KUBICEK",
      "request_type": "register"
    },
    "external_id": "our_customer_invoice_35"
  }
]
```


## Request
Request reprezentuje jeden konkrétní požadavek zákazníka.

### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of request</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>object_type</strong></td>
    <td><em>string</em></td>
    <td>Typ objektu</td>
    <td><code>"domain"</code></td>
  </tr>
  <tr>
    <td><strong>request_type</strong></td>
    <td><em>string</em></td>
    <td>Typ požadavku</td>
    <td><code>"register"</code></td>
  </tr>
  <tr>
    <td><strong>registry_object_name</strong></td>
    <td><em>string</em></td>
    <td>Identifikátor objektu v registru</td>
    <td><code>"KUBICEK"</code></td>
  </tr>
  <tr>
    <td><strong>external_id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor objednávky v systému zákazníka</td>
    <td><code>"our_customer_invoice_35"</code></td>
  </tr>
</table>

### Request Create
Podání nového požadavku.

```
POST /requests
```


#### Curl Example
```term
$ curl -n -X POST /requests \
-H "Content-Type: application/json" \
-d '{}'
```

#### Response Example
```
HTTP/1.1 201 Created
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "object_type": "domain",
  "request_type": "register",
  "registry_object_name": "KUBICEK",
  "external_id": "our_customer_invoice_35"
}
```

### Request Info
Seznam požadavků.

```
GET /requests/{request_id}
```


#### Curl Example
```term
$ curl -n -X GET /requests/$request_id
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "object_type": "domain",
  "request_type": "register",
  "registry_object_name": "KUBICEK",
  "external_id": "our_customer_invoice_35"
}
```

### Request List
Výpis požadavků.

```
GET /requests
```


#### Curl Example
```term
$ curl -n -X GET /requests
```

#### Response Example
```
HTTP/1.1 200 OK
Accept-Range: id
Content-Range: id 01234567-89ab-cdef-0123-456789abcdef..01234567-89ab-cdef-0123-456789abcdef; max=200
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
[
  {
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "object_type": "domain",
    "request_type": "register",
    "registry_object_name": "KUBICEK",
    "external_id": "our_customer_invoice_35"
  }
]
```


