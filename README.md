# CoolCounter-API

API for CoolCounter App

## Install and start the server

```
$ npm install
$ npm start
```

## API endpoints / examples

The following endpoints are expecting a `Content-Type: application/json`

```
GET /api/v1/counters
[
]

POST { title: "Coffee" } /api/v1/counter
[
    { id: "adsf", title: "Coffee", count: 0 }
]

POST { title: "Tea" } /api/v1/counter
[
    { id: "asdf", title: "Coffee", count: 0 },
    { id: "qwer", title: "Tea", count: 0 }
]

POST { id: "asdf" } /api/v1/counter/inc
[
    { id: "asdf", title: "Coffee", count: 1 },
    { id: "qwer", title: "Tea", count: 0 }
]

POST { id: "qwer"} /api/v1/counter/dec
[
    { id: "asdf", title: "Coffee", count: 1 },
    { id: "qwer", title: "Tea", count: -1 }
]

DELETE { id: "qwer" } /api/v1/counter
[
    { id: "asdf", title: "Coffee", count: 1 }
]

GET /api/v1/counters
[
    { id: "asdf", title: "Coffee", count: 1 },
]
```
---
