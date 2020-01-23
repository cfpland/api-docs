# [CFP Land API Documentation](https://cfpland.github.io/api-docs/)

This document outlines the endpoints available for the [CFP Land](https://www.cfpland.com/) conference data API. This repo will also be used to track improvements and changes - including new versions, deprecations, and enhanced functionality, so you might want to [watch on Github](https://github.com/cfpland/api-docs/watchers) if you're actively using this API.

> **Note:** This API is experimental, and subject to change, but I'll try not to introduce any breaking changes to the `/v0/` path.

## Unauthenticated Users

Public, unrestricted access to the CFP Land API includes all conferences with CFPs closing in the next 21 days. This same data is also available via our [RSS Feed or website](https://www.cfpland.com/conferences/).

### Get Conferences

```
GET https://api.cfpland.com/v0/conferences
```

#### Query Params
- `category` One of the 14 following options may be used:
  - .NET
  - CSS
  - Data
  - Design
  - DevOps
  - General
  - Go
  - Java
  - Javascript
  - Mobile
  - PHP
  - Python
  - Ruby
  - Security
- `region` One of the following world regions may be used:
  - Africa
  - Americas
  - Asia
  - Europe
  - Oceania

#### Response

```
{
    "items": [
        {
            "category": "Security",
            "name": "Threat CON",
            "provider": "Airtable",
            "providerId": "recm97rtUzVwM9wsV",
            "region": "Asia",
            "cfp_due_date": "2019-07-05",
            "cfp_start_date": "2019-05-24",
            "cfp_url": "https://threatcon.io/",
            "created_date": "2019-05-24T00:21:25.000Z",
            "country": "Nepal",
            "description": "THREAT CON is a new initiative that aims to facilitate a gateway to standard practices and create a new development within the field of cybersecurity- for developers, security practitioners, IT administrators or anyone interested.",
            "event_end_date": "2019-05-24",
            "event_start_date": "2019-08-29",
            "event_url": "https://threatcon.io/",
            "icon": [
                {
                    "id": "attSRKTYrJxBpzlWo",
                    "url": "https://dl.airtable.com/.attachments/668308f874146e1c4f49db4246498a3f/10ebc5a8/favicon.png",
                    "filename": "favicon.png",
                    "size": 12826,
                    "type": "image/png",
                    "thumbnails": {
                        "small": {
                            "url": "https://dl.airtable.com/.attachmentThumbnails/42d36d13eb00e9803e923d3063ed053f/f7e763e0",
                            "width": 35,
                            "height": 36
                        },
                        "large": {
                            "url": "https://dl.airtable.com/.attachmentThumbnails/193731f06de766cac75ff1e4ff59e57e/c2b6bf4c",
                            "width": 303,
                            "height": 312
                        },
                        "full": {
                            "url": "https://dl.airtable.com/.attachmentThumbnails/559c207c2617d978bd9671369462c9e7/2a6f2a18",
                            "width": 3000,
                            "height": 3000
                        }
                    }
                }
            ],
            "is_new": true,
            "location": "Kathmandu, Bagmati, NP",
            "subregion": "Southern Asia",
            "twitter": "@threat_con",
            "perks_checked": false,
            "perks_list": "❓",
            "travel_covered": false,
            "hotel_covered": false,
            "stipend_covered": false,
            "created_days_back": 0
        }
    ],
    "total": 1
}
```

## Support or Contact

If you believe you've found an error in this documentation or the API itself, please create an issue here in Github. This helps ensure that other users can learn from any problems you encounter and track solutions.
