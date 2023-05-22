---
title: JsonDataLoadOptions.exact_date_time_parse_formats property
linktitle: exact_date_time_parse_formats property
articleTitle: exact_date_time_parse_formats property
second_title: Aspose.Words for Python
description: "JsonDataLoadOptions.exact_date_time_parse_formats property. Gets or sets exact formats for parsing JSON date-time values while loading JSON"
type: docs
weight: 30
url: /python-net/aspose.words.reporting/jsondataloadoptions/exact_date_time_parse_formats/
---

## JsonDataLoadOptions.exact_date_time_parse_formats property

Gets or sets exact formats for parsing JSON date-time values while loading JSON. The default is ``None``.


Strings encoded using Microsoft® JSON date-time format (for example, "/Date(1224043200000)/") are always 
recognized as date-time values regardless of a value of this property. The property defines additional 
formats to be used while parsing date-time values from strings in the following way:


* When [JsonDataLoadOptions.exact_date_time_parse_formats](./) is ``None``, the ISO-8601 format and all date-time formats 
  supported for the current, English USA, and English New Zealand cultures are used additionally in 
  the mentioned order.
  
  
* When [JsonDataLoadOptions.exact_date_time_parse_formats](./) contains strings, they are used as additional date-time
  formats utilizing the current culture.
  
  
* When [JsonDataLoadOptions.exact_date_time_parse_formats](./) is empty, no additional date-time formats are used.
  
  



### See Also

* module [aspose.words.reporting](../../)
* class [JsonDataLoadOptions](../)

