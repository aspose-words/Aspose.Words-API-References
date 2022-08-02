---
title: exact_date_time_parse_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets an exact format for parsing JSON date-time values while loading JSON"
type: docs
weight: 30
url: /python-net/aspose.words.reporting/jsondataloadoptions/exact_date_time_parse_format/
---

## JsonDataLoadOptions.exact_date_time_parse_format property

Gets or sets an exact format for parsing JSON date-time values while loading JSON. The default is **null**.


Strings encoded using Microsoft® JSON date-time format (for example, "/Date(1224043200000)/") are always 
recognized as date-time values regardless of a value of this property. The property defines additional 
formats to be used while parsing date-time values from strings in the following way:


* When [JsonDataLoadOptions.exact_date_time_parse_format](./) is **null**, the ISO-8601 format and all date-time formats 
  supported for the current, English USA, and English New Zealand cultures are used additionally in 
  the mentioned order.
  
  
* When [JsonDataLoadOptions.exact_date_time_parse_format](./) is a non-empty string, it is used as a single additional 
  date-time format utilizing the current culture.
  
  
* When [JsonDataLoadOptions.exact_date_time_parse_format](./) is an empty string, no additional date-time formats are used.
  
  



### See Also

* module [aspose.words.reporting](../../)
* class [JsonDataLoadOptions](../)

