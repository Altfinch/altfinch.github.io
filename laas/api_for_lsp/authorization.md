---
layout: default
title: Authorization
parent: API documentation for LSP
grand_parent: Lending as a Service
nav_order: 1
---

## Authorization

### Description
Retrieve authentication token

### Request
GET
{: .label .label-blue } 

### Route

`/api/v1/auth-token`

### Headers

| Name                 | Description  	                                      |
|:---------------------|:-----------------------------------------------------|
| `x-client-name`      | As provided to you 		                          |
| `x-client-secret`	   | As provided to you									  |

### Parameters

| Name         | Possible values   		   | Required | Description                        |
|:-------------|:--------------------------|:---------|:-----------------------------------|
| `oreos`      | oreos 			   		   | oreos    | oreos                              |

### Response

200
{: .label .label-green } 

```json
{
    "message": "OK",
    "data": {
        "auth_token": "627f9bed55e04dea6a5b1b9ac7bfe951",
        "expiry_in_seconds": 60000
    },
    "errors": null
}
```

400
{: .label .label-red } 

```json
{
    "message": "OK",
    "data": {
        "auth_token": "627f9bed55e04dea6a5b1b9ac7bfe951",
        "expiry_in_seconds": 60000
    },
    "errors": null
}
```



