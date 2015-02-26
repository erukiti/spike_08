## Person resource
人間を表すリソース。ほげほげふがふが。


### Attributes
| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **id** | *uuid* | その人のユニークな識別子<br/> **pattern:** <code>^[0-9a-z]{8}\-[0-9a-z]{4}\-[0-9a-z]{4}\-[0-9a-z]{4}\-[0-9a-z]{12}$</code> | `"01234567-89ab-cdef-0123-456789abcdef"` |
| **firstname** | *regex* | その人のfirstname | `"hoge"` |
| **lastname** | *regex* | その人のlastname | `"fuga"` |
| **created_at** | *date-time* | when person was created | `"2012-01-01T12:00:00Z"` |
| **updated_at** | *date-time* | when person was updated | `"2012-01-01T12:00:00Z"` |
### Person resource Create
person を作成する

```
POST /persons
```

#### Required Parameters
| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **firstname** | *regex* | その人のfirstname | `"hoge"` |
| **lastname** | *regex* | その人のlastname | `"fuga"` |



#### Curl Example
```bash
$ curl -n -X POST /persons \
  -H "Content-Type: application/json" \
 \
  -d '{
  "firstname": "hoge",
  "lastname": "fuga"
}'

```


#### Response Example
```
HTTP/1.1 201 Created
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Person resource Delete
既存の person を削除する

```
DELETE /persons/:id
```


#### Curl Example
```bash
$ curl -n -X DELETE /persons/:id \
  -H "Content-Type: application/json" \

```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Person resource Info
既存の person を取得する

```
GET /persons/:id
```


#### Curl Example
```bash
$ curl -n -X GET /persons/:id

```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### Person resource List
person のリストを取得する

```
GET /persons
```


#### Curl Example
```bash
$ curl -n -X GET /persons

```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
[
  {
    "id": "01234567-89ab-cdef-0123-456789abcdef",
    "firstname": "hoge",
    "lastname": "fuga",
    "created_at": "2012-01-01T12:00:00Z",
    "updated_at": "2012-01-01T12:00:00Z"
  }
]
```

### Person resource Update
person の情報を更新する

```
PUT /persons/:id
```

#### Optional Parameters
| Name | Type | Description | Example |
| ------- | ------- | ------- | ------- |
| **firstname** | *regex* | その人のfirstname | `"hoge"` |
| **lastname** | *regex* | その人のlastname | `"fuga"` |


#### Curl Example
```bash
$ curl -n -X PUT /persons/:id \
  -H "Content-Type: application/json" \
 \
  -d '{
  "firstname": "hoge",
  "lastname": "fuga"
}'

```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```


