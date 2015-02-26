# API
* [Person resource](#person-resource)
 * [POST /persons](#post-persons)
 * [DELETE /persons/:id](#delete-personsid)
 * [GET /persons/:id](#get-personsid)
 * [GET /persons](#get-persons)
 * [PUT /persons/:id](#put-personsid)

## Person resource
人間を表すリソース。ほげほげふがふが。


### Properties
* id
 * その人のユニークな識別子
 * Example: `"01234567-89ab-cdef-0123-456789abcdef"`
 * Type: string
 * Format: uuid
* firstname
 * その人のfirstname
 * Example: `"hoge"`
 * Type: string
 * Format: regex
* lastname
 * その人のlastname
 * Example: `"fuga"`
 * Type: string
 * Format: regex
* created_at
 * when person was created
 * Example: `"2012-01-01T12:00:00Z"`
 * Type: string
 * Format: date-time
* updated_at
 * when person was updated
 * Example: `"2012-01-01T12:00:00Z"`
 * Type: string
 * Format: date-time

### POST /persons
person を作成する

* firstname
 * その人のfirstname
 * Example: `"hoge"`
 * Type: string
 * Format: regex
* lastname
 * その人のlastname
 * Example: `"fuga"`
 * Type: string
 * Format: regex

```
POST /persons HTTP/1.1
Content-Type: application/json
Host: api.example.com

{
  "firstname": "hoge",
  "lastname": "fuga"
}
```

```
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### DELETE /persons/:id
既存の person を削除する

```
DELETE /persons/:id HTTP/1.1
Host: api.example.com
```

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### GET /persons/:id
既存の person を取得する

```
GET /persons/:id HTTP/1.1
Host: api.example.com
```

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

### GET /persons
person のリストを取得する

```
GET /persons HTTP/1.1
Host: api.example.com
```

```
HTTP/1.1 200 OK
Content-Type: application/json

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

### PUT /persons/:id
person の情報を更新する

* firstname
 * その人のfirstname
 * Example: `"hoge"`
 * Type: string
 * Format: regex
* lastname
 * その人のlastname
 * Example: `"fuga"`
 * Type: string
 * Format: regex

```
PUT /persons/:id HTTP/1.1
Content-Type: application/json
Host: api.example.com

{
  "firstname": "hoge",
  "lastname": "fuga"
}
```

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "firstname": "hoge",
  "lastname": "fuga",
  "created_at": "2012-01-01T12:00:00Z",
  "updated_at": "2012-01-01T12:00:00Z"
}
```

