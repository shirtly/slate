# Stores

```shell
curl "http://dayvough.com/v1/stores"
```

Something something about Stores here.

## Get Store

```shell
curl "http://dayvough.com/v1/users/38"
  -H "Authorization: <auth_token>"
```

```json
{
  "data": {
    "id": 38,
    "name": "The 175 Apparel",
    "url": "The175",
    "description": "Mayroon tayong 175 na mga wika sa Pilipinas. Sama-sama nating pangalagaan ang mga ito. We're a Filipino Apparel that lets you Wear Your Wika!",
    "created_at": "2015-07-12T11:09:51.000Z",
    "updated_at": "2016-06-27T11:58:42.289Z",
    "v3_store_id": 61,
    "profits": 12345,
    "sales": 234567
  },
  "products": [
    {
      "id": 159,
      "name": "Tadhana White",
      "description": "(n.) destiny, the predetermined or inevitable course of events... also the top grossing Filipino Indie film full of timeless hugot lines. This shirt is a That Thing Called Tadhana-inspired shirt from our Filipino Apparel.",
      "v3_product_id": 187,
      "uuid": null,
      "ordered": false,
      "product_type": null,
      "material": null,
      "print_style": null,
      "mockup": "/uploads/product/187/tadhana-white.jpg",
      "file": null,
      "size": null,
      "color": null,
      "cost_base": 250,
      "cost_total": 399,
      "created_at": "2016-02-28T02:39:25.000Z",
      "updated_at": "2016-06-27T12:03:00.852Z",
      "user_id": 76
    }
  ]
}
```

This endpoint retrieves a specific store.

### HTTP Request

`GET http://dayvough.com/v1/stores/<store_id>`

### Store Data

Attribute | Type    | Description
--------- | ------- | -----------
id | integer | Stores's id
name | string | Store's display name
url | string | Store's URL link <br> (Only accepts alphanumeric URLs)









