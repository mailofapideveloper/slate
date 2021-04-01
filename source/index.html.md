---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript

toc_footers:
  - <a href='#'>For any question please reachout to Lokitos <ML.DIGITAL.WSAG.SUPPORT@heb.com></a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the HEB Developer API Site! You can use our API to access Product details and store information.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.



# Authentication

> To authorize, use this code:


```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "apikey: your_apikey"
```

```python
import apihub

api = apihub.authorize('your_apikey')
```

```javascript
const apihub = require('apihub');

let api = apihub.authorize('your_apikey');
```



> Make sure to replace `your_apikey` with the actual API key.

H-E-B uses API keys to allow access to the API's.

H-E-B expects for the API key to be included in all API requests to the server in a header that looks like the following:

`apikey: your_apikey`

<aside class="notice">
You must replace <code>your_apikey</code> with your personal API key.
</aside>

# Stores

## Get All Stores


```shell
curl "https://openapi.uat.heb.com/apihub/v1/stores"
  -H "apikey: your_apikey"
```

```javascript
const store = require('store');

let api = stores.authorize('your_apikey');
let stores = api.stores.get();
```

```python
import store

api = store.authorize('your_apikey')
api.stores.get()
```

> The above command returns JSON structured like this:

```json
{
   "stores": [ 
    {
       "storeNumber": 1,
       "name": "Elizabeth and 9th Street H-E-B",
	   "locationTypeCode": "S",
	   "locationName": "BR01 ELIZABETH",
       "loc_abb": "BRO 1",
       "latitude": 25.90281,
       "longitude": -97.50018,
       "address": "924 SE ELIZABETH",
       "city": "BROWNSVILLE",
       "state": "TX",
       "zip": "78520-5147",
       "storePhone": " (956) 542-4191",
       "ecommOpenDate": "",
       "ecommcloseDate": "",
       "hasPharmacy": false,
       "spanishPrintable": false,
       "storeHours": "Mon-Sun 07:00 AM - 09:00 PM",
       "active": true,
       "taxDivisionId": 1,
       "taxPercentage": 0.0825,
       "companyId": 1,
       "companyName": "HEB GROCERY COMPANY",
       "lobId": 1,
       "lobName": "SA FOOD/DRUG",
       "districtId": 82,
       "districtName": "BORDER/LOWER VALLEY",
       "financialDivId": 1,
       "financialDivName": "BORDER",
       "mktRegionId": 82,
       "mktRegionName": "PRICE ZONE 82",
       "openedDate": "03/11/1958",
       "closedDate": "01/01/1600",
       "retailLocFormatCode": "NP",
       "retailLocFormatDesc": "Non-plus",
       "mapPlaceId": "",
       "retailLocSegmentCd": "V",
       "retailLocSegmentDesc": "Value",
       "events": [ 
        {
           "id": 40,
           "active": false,
           "priority": "",
           "name": "Taco Revolucion",
           "description": "",
           "pageURL": "https://www.heb.com/static-page/taco-revolucion",
           "displayStartDate": "",
           "displayEndDate": "",
           "dates": "" 
        },
        {
           "id": 65,
           "active": false,
           "priority": "",
           "name": "Game Day Recipe Faceoff",
           "description": "",
           "pageURL": "https://www.heb.com/static-page/All-Star-Tailgating",
           "displayStartDate": "",
           "displayEndDate": "",
           "dates": "" 
        },
      ],
       "areas": [ 
        {
           "id": 16,
           "name": "Meat Market",
           "feature": [ 
            {
               "id": 4,
               "name": "Custom Meat Cutting" 
            } 
          ] 
        },
         
        {
           "id": 17,
           "name": "Produce" 
        },
         
        {
           "id": 13,
           "name": "Drug and General Merchandise" 
        },
         
        {
           "id": 19,
           "name": "Seafood",
           "feature": [ 
            {
               "id": 4,
               "name": "Gulf Shrimp" 
            } 
          ] 
        },
         
        {
           "id": 12,
           "name": "Grocery" 
        } 
      ],
       "storeFulfillment": [ 
        {
           "fulfillmentChannelName": "Pick up in Store",
           "fulfillmentChannelCode": "01",
           "fulfillmentChannelEffectiveDate": "01/01/1600",
           "storeHours": 
          {
             "monday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "tuesday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "wednesday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "thursday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "friday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "saturday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            },
             "sunday": 
            {
               "openHour": "08:00 AM",
               "closeHour": "08:00 PM" 
            } 
          } 
        } 
      ],
       "productTypeFulfillment": [ 
        {
           "fulfillmentChannelName": "Pick up in Store",
           "departmentName": "06E",
           "blackoutDates": [ "10/25/2018",
             "10/26/2018",
             "10/27/2018",
             "10/28/2018",
          ],
           "pickupHours": "Mon 11:00 AM - 06:00 PM,
          Tue-Sun 11:00 AM - 08:00 PM" 
        } 
      ] 
    },
    {
       "storeNumber": 2,
       "name": "Farragut and Flores H-E-B",
	   "locationTypeCode": "S",
	   "locationName": "LAR01 FARRAGUT/FLORES",
       "loc_abb": "LAR 1",
       "latitude": 27.506,
       "longitude": -99.5061,
       "address": "1002 FARRAGUT",
       "city": "LAREDO",
       "state": "TX",
       "zip": "78040-5017",
       "storePhone": " (956) 791-3571",
       "ecommOpenDate": "",
       "ecommcloseDate": "06/26/2016",
       "hasPharmacy": false,
       "spanishPrintable": true,
       "storeHours": "Mon-Fri 07:00 AM - 10:00 PM, Sat 07:00 AM - 07:00 AM, Sun 10:00 PM - 10:00 PM",
       "active": false,
       "taxDivisionId": 1,
       "taxPercentage": 0.0825,
       "companyId": 1,
       "companyName": "HEB GROCERY COMPANY",
       "lobId": 1,
       "lobName": "SA FOOD/DRUG",
       "districtId": 83,
       "districtName": "BORDER/SOUTHWEST",
       "financialDivId": 1,
       "financialDivName": "BORDER",
       "mktRegionId": 83,
       "mktRegionName": "PRICE ZONE 83",
       "openedDate": "10/01/1992",
       "closedDate": "06/26/2016",
       "retailLocFormatCode": "NP",
       "retailLocFormatDesc": "Non-plus",
       "mapPlaceId": "",
       "retailLocSegmentCd": "V",
       "retailLocSegmentDesc": "Value",
       "events": [ 
        {
           "id": 40,
           "active": false,
           "priority": "",
           "name": "Taco Revolucion",
           "description": "",
           "pageURL": "https://www.heb.com/static-page/taco-revolucion",
           "displayStartDate": "",
           "displayEndDate": "",
           "dates": "" 
        },
        {
           "id": 117,
           "active": false,
           "priority": "",
           "name": "Pepper Mania",
           "description": "",
           "pageURL": "https://www.heb.com/pepper",
           "displayStartDate": "",
           "displayEndDate": "",
           "dates": "" 
        },
      ],
       "areas": [ 
        {
           "id": 12,
           "name": "Grocery" 
        },
         
        {
           "id": 19,
           "name": "Seafood" 
        },
         
        {
           "id": 17,
           "name": "Produce" 
        },
         
        {
           "id": 16,
           "name": "Meat Market" 
        },
         
        {
           "id": 13,
           "name": "Drug and General Merchandise" 
        },
         
        {
           "id": 18,
           "name": "Bakery",
           "feature": [ 
            {
               "id": 1,
               "name": "Bakery" 
            } 
          ] 
        } 
      ] 
    }
	...
  ]
}
```

This endpoint retrieves details of all Stores.

### HTTP Request

`GET https://openapi.uat.heb.com/apihub/v1/stores`

### Request Parameters

Name | Type | Required | Description
---- | ---- | -------- | -----------
apiKey | HTTP Header | required | API access key.


<aside class="success">
Remember — To get a successful response, you must send a valid apikey !
</aside>

## Get a Specific Store Details



```shell
curl "https://openapi.uat.heb.com/apihub/v1/stores/182"
  -H "apikey:your_apikey"
```

```javascript
const store = require('store');

let api = stores.authorize('your_apikey');
let stores = api.stores.get(182);
```

```python
import store

api = store.authorize('your_apikey')
api.stores.get(182)
```


> The above command returns JSON structured like this:

```json
{
    "storeNumber": 182,
    "name": "31st and Market H-E-B",
    "locationTypeCode": "S",
    "locationName": "TEMPLE 02 31ST/LOOP 363",
    "loc_abb": "TEMP2",
    "latitude": 31.07223,
    "longitude": -97.37061,
    "address": "3002 S 31TH ST",
    "city": "TEMPLE",
    "state": "TX",
    "zip": "76502-1802",
    "storePhone": " (254) 778-4820",
    "ecommOpenDate": "05/20/2018",
    "ecommcloseDate": "",
    "hasPharmacy": true,
    "spanishPrintable": false,
    "storeHours": "Mon-Sun 12:00 AM  - 12:00 AM",
    "active": true,
    "taxDivisionId": 1.0,
    "taxPercentage": 0.0825,
    "companyId": 1.0,
    "companyName": "HEB GROCERY COMPANY",
    "lobId": 1.0,
    "lobName": "SA FOOD/DRUG",
    "districtId": 9.0,
    "districtName": "NORTH AREA",
    "financialDivId": 3.0,
    "financialDivName": "CNTRL TEXAS",
    "mktRegionId": 9.0,
    "mktRegionName": "PRICE ZONE 9",
    "openedDate": "10/21/1980",
    "closedDate": "01/01/1600",
    "retailLocFormatCode": "NP",
    "retailLocFormatDesc": "Non-plus",
    "mapPlaceId": "",
    "retailLocSegmentCd": "C",
    "retailLocSegmentDesc": "Core",
    "events": [
        {
            "id": 3,
            "active": false,
            "priority": "",
            "name": "Shrimp Boil",
            "description": "Come enjoy fresh Gulf shrimp cook right in front of you",
            "pageURL": "guide-san-antonio-463.pdf",
            "displayStartDate": "",
            "displayEndDate": "",
            "dates": ""
        },
        {
            "id": 37,
            "active": false,
            "priority": "",
            "name": "test event 256 size",
            "description": "",
            "pageURL": "",
            "displayStartDate": "",
            "displayEndDate": "",
            "dates": ""
        }
    ],
    "areas": [
        {
            "id": 12,
            "name": "Grocery"
        },
        {
            "id": 13,
            "name": "Drug and General Merchandise",
            "feature": [
                {
                    "id": 9,
                    "name": "Beauty"
                }
            ]
        },
        {
            "id": 14,
            "name": "Flower Shop",
            "feature": [
                {
                    "id": 6,
                    "name": "Floral"
                },
                {
                    "id": 2,
                    "name": "Wedding Service"
                }
            ]
        },
        {
            "id": 18,
            "name": "Bakery",
            "feature": [
                {
                    "id": 4,
                    "name": "Scratch Bakery"
                },
                {
                    "id": 1,
                    "name": "Bakery"
                },
                {
                    "id": 3,
                    "name": "Tortilleria"
                }
            ]
        },
        {
            "id": 19,
            "name": "Seafood",
            "feature": [
                {
                    "id": 2,
                    "name": "Sushi"
                },
                {
                    "id": 5,
                    "name": "Salmon Burgers"
                },
                {
                    "id": 4,
                    "name": "Gulf Shrimp"
                },
                {
                    "id": 1,
                    "name": "Fish Market"
                }
            ]
        },
        {
            "id": 20,
            "name": "Deli",
            "feature": [
                {
                    "id": 6,
                    "name": "Deli"
                }
            ]
        },
        {
            "id": 22,
            "name": "Online Services",
            "feature": [
                {
                    "id": 3,
                    "name": "Curbside"
                },
                {
                    "id": 4,
                    "name": "Delivery"
                }
            ]
        },
        {
            "id": 21,
            "name": "Store Services",
            "feature": [
                {
                    "id": 5,
                    "name": "Bissell Green Carpet Cleaner"
                },
                {
                    "id": 11,
                    "name": "Open 24 Hours"
                },
                {
                    "id": 6,
                    "name": "Coin Star"
                },
                {
                    "id": 4,
                    "name": "Business Center"
                }
            ]
        },
        {
            "id": 17,
            "name": "Produce",
            "feature": [
                {
                    "id": 4,
                    "name": "Fresh Guacamole"
                },
                {
                    "id": 3,
                    "name": "Juicing"
                }
            ]
        },
        {
            "id": 11,
            "name": "Pharmacy",
            "feature": [
                {
                    "id": 2,
                    "name": "Drive Thru"
                },
                {
                    "id": 3,
                    "name": "Compounding"
                },
                {
                    "id": 5,
                    "name": "Immunizations"
                },
                {
                    "id": 7,
                    "name": "Pharmacy"
                }
            ]
        },
        {
            "id": 16,
            "name": "Meat Market",
            "feature": [
                {
                    "id": 8,
                    "name": "Organic Meat"
                },
                {
                    "id": 3,
                    "name": "Full Service Butcher Case"
                },
                {
                    "id": 7,
                    "name": "Grass Fed Beef"
                },
                {
                    "id": 6,
                    "name": "Prime Beef"
                },
                {
                    "id": 4,
                    "name": "Custom Meat Cutting"
                }
            ]
        }
    ],
    "storeFulfillment": [
        {
            "fulfillmentChannelName": "Pick up in Store",
            "fulfillmentChannelCode": "01",
            "fulfillmentChannelEffectiveDate": "01/01/1600",
            "storeHours": {
                "monday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "tuesday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "wednesday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "thursday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "friday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "saturday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                },
                "sunday": {
                    "openHour": "08:00 AM",
                    "closeHour": "08:00 PM"
                }
            }
        },
        {
            "fulfillmentChannelName": "Curbside Pickup",
             "fulfillmentChannelCode": "06",
            "fulfillmentChannelEffectiveDate": "05/20/2018",
            "storeHours": {
                "monday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "tuesday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "wednesday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "thursday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "friday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "saturday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                },
                "sunday": {
                    "openHour": "07:30 AM",
                    "closeHour": "09:00 PM"
                }
            }
        }
    ],
    "productTypeFulfillment": [
        {
            "fulfillmentChannelName": "Pick up in Store",
            "departmentName": "06A",
            "blackoutDates": [
                "11/26/2015",
                "12/25/2015",
                "03/27/2016",
                "11/24/2016",
                "12/25/2016",
                "04/16/2017",
                "11/23/2017",
                "12/25/2017",
                "04/01/2018",
                "12/25/2018"
            ],
            "pickupHours": "Mon-Sun 08:00 AM  - 08:00 PM"
        },
        {
            "fulfillmentChannelName": "Pick up in Store",
            "departmentName": "09F",
            "blackoutDates": [
                "11/26/2015",
                "03/27/2016",
                "11/24/2016",
                "12/25/2016",
                "04/16/2017",
                "11/23/2017",
                "12/25/2017",
                "04/01/2018",
                "12/25/2018"
            ],
            "pickupHours": "Mon-Sun 08:00 AM  - 08:00 PM"
        }
    ]
}
```

This endpoint retrieves a specific store details.


### HTTP Request

`GET https://openapi.uat.heb.com/apihub/v1/stores/<storeNum>`

### Request Parameters

Name | Type | Required | Description
---- | ---- | -------- | -----------
apiKey | HTTP Header | required | API access key.
storeNum | string | required | ID for a specific store.


## Store FilterSearch
This endpoint returns information from multiples stores

```shell
curl "https://openapi.uat.heb.com/apihub/v1/stores/filterSearch"
  -X POST
  -H "apikey:your_apikey"
  -d '{"stores":{"fields":["storeNumber","locationName","locationTypeCode","events.name","events" ],"storeNbr":[1,150]}}'
```

> The above command returns JSON structured like this:

```json
{
    "stores": [
        {
            "storeNumber": 1,
            "locationName": "BR01 ELIZABETH",
            "locationTypeCode": "S",
            "events": [
                {
                    "displayStartDate": "",
                    "name": "Taco Revolucion",
                    "active": false,
                    "description": "",
                    "pageURL": "https://www.heb.com/static-page/taco-revolucion",
                    "dates": "",
                    "id": 40,
                    "priority": "",
                    "displayEndDate": ""
                }
            ]
        },
        {
            "storeNumber": 150,
            "locationName": "EAGLE PASS 2",
            "locationTypeCode": "S"
        }
    ]
}
```

### HTTP Request

`POST https://openapi.uat.heb.com/apihub/v1/stores/filterSearch`

### Request Parameters

Name | Type | Required | Description
---- | ---- | -------- | -----------
apiKey | HTTP Header | required | API access key.
stores | body | required | List of stores to search for and list of fields to return.
bodyFields | string | storeNbr required | storeNbr, fields

<aside class="success">
Store Numbers are included in the request body!
</aside>



# APIKeyLookup

## GetMatchingKey
To Query the application name based on last 4 characters of the apikey , The response will have a JSON object with Application Details(appName,apikey and Status)

```python
import apikeylookup

api = apikeylookup.authorize('your_apikey')
api.apikeylookup.get()
```

```shell
curl "http://openapi.uat.heb.com/REST/v1/apiKeyLookup/getMatchingKey?apikey=f17b`" \
  -H "apikey: your_apikey"
```

```javascript
const apikeylookup = require('apikeylookup');

let api = apikeylookup.authorize('your_apikey');
let apikeylookup = api.apikeylookup.get();
```
> The above command returns JSON structured like this:

```json
{
    "appName": "Lokitos Test Application",
    "apiKey": "l7xx7f28414e1eb34dadjrhdu83hrgd8f17b",
    "status": "active"
}
```
This endpoint retrieves the Application details.

<aside class="notice">
Use atleast last 4 characters to get the matching key.
</aside>

### HTTP Request
`GET http://openapi.uat.heb.com/REST/v1/apiKeyLookup/getMatchingKey?apikey=f17b`
### Request Parameters

Name | Type | Required | Description
---- | ---- | -------- | -----------
apiKey | string | required | partial apikey

## GetKeyDetails
To get the application details using the complete API Key, Response will have a JSON object with application details

```python
import apikeylookup

api = apikeylookup.authorize('your_apikey')
api.apikeylookup.get()
```

```shell
curl "http://openapi.uat.heb.com/REST/v1/apiKeyLookup/getKeyDetails?apikey=l7xx7f28414e1eb34dadjrhdu83hrgd8f17b`" \
  -H "apikey: your_apikey"
```

```javascript
const apikeylookup = require('apikeylookup');

let api = apikeylookup.authorize('your_apikey');
let apikeylookup = api.apikeylookup.get();
```
> The above command returns JSON structured like this:

```json
{
    "App": "Lokitos Test Application",
    "org": "Digital Engineering",
    "status": "active"
}
```
This endpoint retrieves the Application details.
### HTTP Request

`GET http://openapi.uat.heb.com/REST/v1/apiKeyLookup/getKeyDetails?apikey=l7xx7f28414e1eb34dadjrhdu83hrgd8f17b`

### Request Parameters
Name | Type | Required | Description
---- | ---- | -------- | -----------
apiKey | string | required | full apikey