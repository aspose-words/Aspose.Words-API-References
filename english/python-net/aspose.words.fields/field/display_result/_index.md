---
title: Field.display_result property
linktitle: display_result property
articleTitle: display_result property
second_title: Aspose.Words for Python
description: "Field.display_result property. Gets the text that represents the displayed field result."
type: docs
weight: 10
url: /python-net/aspose.words.fields/field/display_result/
---

## Field.display_result property

Gets the text that represents the displayed field result.


```python
@property
def display_result(self) -> str:
    ...

```

### Remarks

The [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) method must be called to obtain correct value for the
[FieldListNum](../../fieldlistnum/), [FieldAutoNum](../../fieldautonum/), [FieldAutoNumOut](../../fieldautonumout/) and [FieldAutoNumLgl](../../fieldautonumlgl/) fields.



### Examples

Shows how to get the real text that a field displays in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("This document was written by ")
field_author = builder.insert_field(aw.fields.FieldType.FIELD_AUTHOR, True).as_field_author()
field_author.author_name = "John Doe"

# We can use the "display_result" property to verify what exact text
# a field would display in its place in the document.
self.assertEqual("", field_author.display_result)

# Fields do not maintain accurate result values in real-time.
# To make sure our fields display accurate results at any given time,
# such as right before a save operation, we need to update them manually.
field_author.update()

self.assertEqual("John Doe", field_author.display_result)

doc.save(ARTIFACTS_DIR + "Field.display_result.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

