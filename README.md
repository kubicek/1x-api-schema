## Order


### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>created_at</strong></td>
    <td><em>date-time</em></td>
    <td>when order was created</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of order</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>updated_at</strong></td>
    <td><em>date-time</em></td>
    <td>when order was updated</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
</table>

### Order Create
Create a new order.

```
POST /orders
```


#### Curl Example
```term
$ curl -n -X POST /orders \
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
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Order Delete
Delete an existing order.

```
DELETE /orders/{order_id}
```


#### Curl Example
```term
$ curl -n -X DELETE /orders/$order_id
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Order Info
Info for existing order.

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
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Order List
List existing orders.

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
    "created_at": "2012-01-01T12:00:00Z",
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "updated_at": "2012-01-01T12:00:00Z"
  }
]
```

### Order Update
Update an existing order.

```
PATCH /orders/{order_id}
```


#### Curl Example
```term
$ curl -n -X PATCH /orders/$order_id \
-H "Content-Type: application/json" \
-d '{}'
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```


## Request


### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>created_at</strong></td>
    <td><em>date-time</em></td>
    <td>when request was created</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of request</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>updated_at</strong></td>
    <td><em>date-time</em></td>
    <td>when request was updated</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
</table>

### Request Create
Create a new request.

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
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Request Delete
Delete an existing request.

```
DELETE /requests/{request_id}
```


#### Curl Example
```term
$ curl -n -X DELETE /requests/$request_id
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Request Info
Info for existing request.

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
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Request List
List existing requests.

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
    "created_at": "2012-01-01T12:00:00Z",
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "updated_at": "2012-01-01T12:00:00Z"
  }
]
```

### Request Update
Update an existing request.

```
PATCH /requests/{request_id}
```


#### Curl Example
```term
$ curl -n -X PATCH /requests/$request_id \
-H "Content-Type: application/json" \
-d '{}'
```

#### Response Example
```
HTTP/1.1 200 OK
ETag: "0123456789abcdef0123456789abcdef"
RateLimit-Remaining: 1200
```
```javascript```
{
  "created_at": "2012-01-01T12:00:00Z",
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "updated_at": "2012-01-01T12:00:00Z"
}
```


