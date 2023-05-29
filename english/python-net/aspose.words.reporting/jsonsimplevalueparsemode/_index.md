---
title: JsonSimpleValueParseMode enumeration
linktitle: JsonSimpleValueParseMode enumeration
articleTitle: JsonSimpleValueParseMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.reporting.JsonSimpleValueParseMode enumeration. Specifies a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON"
type: docs
weight: 50
url: /python-net/aspose.words.reporting/jsonsimplevalueparsemode/
---

## JsonSimpleValueParseMode enumeration

Specifies a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. 
Such a mode does not affect parsing of date-time values.


### Members

| Name | Description |
| --- | --- |
| LOOSE | Specifies the mode where types of JSON simple values are determined upon parsing of their string representations. For example, the type of 'prop' from the JSON snippet '{ prop: "123" }' is determined as integer in this mode. |
| STRICT | Specifies the mode where types of JSON simple values are determined from JSON notation itself. For example, the type of 'prop' from the JSON snippet '{ prop: "123" }' is determined as string in this mode. |

### See Also

* module [aspose.words.reporting](../)

