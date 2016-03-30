---
category: Products
path: '/products/search?searchValue=:searchValue'
title: 'Get products by search value'
type: 'GET'

layout: nil
---

This method allows users to get a product by search value

### Request

* ```:searchValue``` is the value of the product to match.
* The headers must include a **valid authentication token**.

```Authentication: bearer TOKEN```

### Response

**If succeeds**, returns array of products that match the search value.

Example of a successful response containing two products:

```Status: 200 OK```
```[
  {
    "Id":682919,
	"CreatedOn":"2015-10-02T10:44:11.9248046",
	"ModifiedOn":"2015-10-02T10:44:11.9248046",
	"Name":"SB INDUSTRIAL RAL4002 VIOLET/ROOD",
	"ImagePath":null,
	"IsActive":true,
	"IsFeatured":false,
	"ProductNumber":"176-01D07117-0400",
	"Description":"SB INDUSTRIAL RAL4002 VIOLET/ROOD",
	"Group":1761,
	"Unit":"0,4 LTR",
	"GrossPrice":13.85,
	"RecommendedRetailPrice":16.76,
	"EanCode":"8711347128396"
  },{
	"Id":682922,
	"CreatedOn":"2015-10-02T10:44:11.9248046",
	"ModifiedOn":"2015-10-02T10:44:11.9248046",
	"Name":"SB INDUSTRIAL RAL4004 BORDEAUXVIOLET",
	"ImagePath":null,
	"IsActive":true,
	"IsFeatured":false,
	"ProductNumber":"176-01D07122-0400",
	"Description":"SB INDUSTRIAL RAL4004 BORDEAUXVIOLET",
	"Group":1761,
	"Unit":"0,4 LTR",
	"GrossPrice":13.85,
	"RecommendedRetailPrice":16.76,
	"EanCode":"8711347071227"
  }
]```

For errors responses, see the [response status codes documentation](#/response-status-codes).
