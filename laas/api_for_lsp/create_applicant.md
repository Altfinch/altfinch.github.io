---
layout: default
title: Create applicant
parent: API documentation for LSP
grand_parent: Lending as a Service
nav_order: 1
---

## Create Applicant

### Description
Create loan applicant

### Request
POST
{: .label .label-yellow} 

### Route

`/api/v1/applicant`

### Headers

| Name                 | Description  	                                      |
|:---------------------|:-----------------------------------------------------|
| `x-client-name`      | As provided to you 		                          |
| `x-client-secret`	   | As provided to you									  |

### Parameters

| Name         | Possible values   		   | Required | Description                        |
|:-------------|:--------------------------|:---------|:-----------------------------------|
| `aadhaar_number`| | 12 digit number | true | Valid UID number as on AADHAAR card|
| `pan_number`| 10 character alphanumeric code | true | Valid PAN number as on PAN card|
|`first_name`| Only alphabets |true | |
|`last_name`| Only alphabets |true | |
|`gender`| M,F|true||
|`date_of_birth`| Valid date |true| |
|`mobile`| 10 digit numeric code| true ||
|`email`| Valid email id| false ||
|`addr_fld_1`| text | true |Valid address length should be between 2 and 100 characters|
|`addr_fld_2`| text | true |Valid address length should be between 2 and 100 characters|
|`pincode`| 6 digit numeric code| true ||


### Response

200
{: .label .label-green } 

```json
{
    "message": "OK",
    "data": {
        "applicant_id": "68a43cfb-40b3-4859-9d3b-578b641ab1df",
        "aadhaar_number": "XXXX XXXX 6611",
        "date_of_birth": "1990-02-20",
        "email": "emk@gmail.com",
        "existing": false,
        "first_name": "Ramesh",
        "gender": "M",
        "last_name": "Kabra",
        "mobile": "9826216710",
        "pan_number": "MXXXXXX5D"
    },
    "errors": null
}
```

400
{: .label .label-red } 

```json
{
    "message": "Bad Request",
    "data": null,
    "errors": {
        "aadhaar_number": [
            "is not a number",
            "can't be blank",
            "is the wrong length (should be 12 characters)"
        ],
        "date_of_birth": [
            "Date needs to be in YYYY-MM-DD",
            "can't be blank"
        ],
        "gender": [
            "can't be blank"
        ],
        "addr_fld_1": [
            "can't be blank",
            "is too short (minimum is 2 characters)"
        ],
        "addr_fld_2": [
            "can't be blank",
            "is too short (minimum is 2 characters)"
        ]
    }
}
```



