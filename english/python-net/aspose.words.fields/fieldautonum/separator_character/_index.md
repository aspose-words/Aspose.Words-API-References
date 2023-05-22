---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Each AUTONUM field displays the current value of a running count of AUTONUM fields,
# allowing us to automatically number items like a numbered list.
# This field will display a number "1.".
field = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_NUM, True).as_field_auto_num()
builder.writeln("\tParagraph 1.")

self.assertEqual(" AUTONUM ", field.get_field_code())

field = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_NUM, True).as_field_auto_num()
builder.writeln("\tParagraph 2.")

# The separator character, which appears in the field result immediately after the number, is a full stop by default.
# If we leave this property null, our second AUTONUM field will display "2." in the document.
self.assertIsNone(field.separator_character)

# We can set this property to apply the first character of its string as the new separator character.
# In this case, our AUTONUM field will now display "2:".
field.separator_character = ":"

self.assertEqual(" AUTONUM  \\s :", field.get_field_code())

doc.save(ARTIFACTS_DIR + "Field.field_auto_num.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

