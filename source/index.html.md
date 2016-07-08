---
title: shirt.ly API v1

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - roles
  - users
  - stores
  - errors
  - v3

search: true
---

# Introduction

```json
{
  "hello world": "git gud"
}
```

Dis be the shirtly-api docs.

# Authentication

> To authorize, use this code:

```shell
curl "http://dayvough.com/auth"
  -H "Authorization: <auth_token>"
```

> Be sure to replace `auth_token` with your API key.

The shirtly-api expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <auth_token>`

<aside class="notice">
You must replace <code>&lt;auth_token&gt;</code> with your personal API key.
</aside>



