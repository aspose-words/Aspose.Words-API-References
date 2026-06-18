---
title: BuiltInDocumentProperties.last_printed property
linktitle: last_printed property
articleTitle: last_printed property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.last_printed property. Gets or sets the date when the document was last printed in UTC."
type: docs
weight: 160
url: /python-net/aspose.words.properties/builtindocumentproperties/last_printed/
---

## BuiltInDocumentProperties.last_printed property

Gets or sets the date when the document was last printed in UTC.


```python
@property
def last_printed(self) -> datetime.datetime:
    ...

@last_printed.setter
def last_printed(self, value: datetime.datetime):
    ...

```

### Remarks

For documents originated from RTF format this property returns the local time of last print operation.

If the document was never printed, this property will return DateTime.MinValue.

Aspose.Words does not update this property.




### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

