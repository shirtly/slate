# Users

```shell
API Endpoint: "http://dayvough.com/v1/users"
```

Something something about Users here.

## Get User

```shell
curl "http://dayvough.com/v1/users/1"
  -H "Authorization: <auth_token>"
```

```json
{
  "data": {
    "id": 1,
    "email": "david@shirt.ly",
    "first_name": "David",
    "last_name": "Marquez",
    "number": "09174223311",
    "referrer": null,
    "v3_user_id": "1",
    "created_at": "2015-09-04T09:40:52.000Z",
    "updated_at": "2016-07-08T09:24:30.518Z",
    "role": "admin"
  },
  "type": "User",
  "relationships": {
    "stores": [
      {
        "id": 180,
        "name": "dayvough",
        "url": "dayvough"
      }
    ],
    "products": [
      {
        "id": 3459,
        "name": "Test23"
      }
    ],
    "orders": [
      {
        "id": 2311
      }
    ]
  },
  "versions": [
    {
      "id": 18596,
      "event": "auth",
      "whodunnit": "unknown"
    }
  ]
}
```

This endpoint retrieves a specific user.

### HTTP Request

`GET http://dayvough.com/v1/users/<user_id>`

### User Data

Attribute | Type    | Description
--------- | ------- | -----------
id | integer | User's unique V4 id
email | string | User's email <br> (Must be unique and matches <code>/\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\z/</code>)
first_name | string | User's first name
last_name | string | User's last name
number | string | User's number
referrer | string | Person who referred user
role | string | User's role <br> (if user is both <code>admin</code> and <code>partner</code>, it stays as <code>admin</code>)


### Relationships

Object | Description
------ | -----------
stores | A list of all of the user's stores
products | A list of all of the user's products
orders | A list of all of the user's orders

### Versions

Displays a list of the 5 latest events of the user.

<!-- ### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve -->

## Get All Users

```shell
curl "http://dayvough.com/v1/users"
  -H "Authorization: <auth_token>"
```

```json
{
  "data": [
    {
      "id": 2,
      "email": "david.marquez@icloud.com",
      "first_name": "Test ",
      "last_name": "Subject",
      "number": null,
      "referrer": null,
      "v3_user_id": 2,
      "created_at": "2015-05-15T08:10:05.000Z",
      "updated_at": "2016-06-27T11:37:06.968Z",
      "role": "admin"
    },
    {
      "id": 3,
      "email": "josh@shirt.ly",
      "first_name": "Joshua",
      "last_name": "Ramos",
      "number": "091712345678",
      "referrer": null,
      "v3_user_id": 3,
      "created_at": "2015-05-15T10:31:30.000Z",
      "updated_at": "2016-06-27T11:37:07.121Z",
      "role": "unassigned"
    },
    ...
  ],
  "links": {
    "self": "http://dayvough.com/v1/users",
    "last": "http://dayvough.com/v1/users/page/10",
    "next": "http://dayvough.com/v1/users/page/2"
  }
}
```

This endpoint retrieves all users.

### HTTP Request

`GET http://dayvough.com/v1/users`

<aside class="notice">
This route is only available for <code>admins</code> and <code>interns</code>
</aside>



