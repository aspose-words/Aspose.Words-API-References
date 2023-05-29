---
title: FieldOptions.legacy_number_format property
linktitle: legacy_number_format property
articleTitle: legacy_number_format property
second_title: Aspose.Words for Python
description: "FieldOptions.legacy_number_format property. Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not."
type: docs
weight: 150
url: /python-net/aspose.words.fields/fieldoptions/legacy_number_format/
---

## FieldOptions.legacy_number_format property

Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

When this property is set to ``True``, template symbol "#" worked as in .net:
Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to ``False``, template symbol "#" works as MS Word:
This format item specifies the requisite numeric places to display in the result.
If the result does not include a digit in that place, MS Word displays a space. For example, { = 9 + 6 \\# $### } displays $ 15.

The default value is ``False``.




### Examples

Shows how enable legacy number formatting for fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field("= 2 + 3 \\# $##")

self.assertEqual("$ 5", field.result)

doc.field_options.legacy_number_format = True
field.update()

self.assertEqual("$5", field.result)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

