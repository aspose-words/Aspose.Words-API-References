---
title: ReportBuilderOptions.missing_member_message property
linktitle: missing_member_message property
articleTitle: missing_member_message property
second_title: Aspose.Words for Python
description: "ReportBuilderOptions.missing_member_message property. Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/reportbuilderoptions/missing_member_message/
---

## ReportBuilderOptions.missing_member_message property

Gets or sets a string value printed instead of a template expression that represents a plain reference to
a missing member of an object. The default value is an empty string.


```python
@property
def missing_member_message(self) -> str:
    ...

@missing_member_message.setter
def missing_member_message(self, value: str):
    ...

```

### Remarks

The property should be used in conjunction with the [ReportBuildOptions.ALLOW_MISSING_MEMBERS](../../../aspose.words.reporting/reportbuildoptions/#ALLOW_MISSING_MEMBERS)
option. Otherwise, an exception is thrown when a missing member of an object is encountered.


The property affects only printing of a template expression representing a plain reference to a missing
object member. For example, printing of a binary operator, one of which operands references a missing
object member, is not affected.

The value of this property cannot be set to null.




### See Also

* module [aspose.words.lowcode](../../)
* class [ReportBuilderOptions](../)

