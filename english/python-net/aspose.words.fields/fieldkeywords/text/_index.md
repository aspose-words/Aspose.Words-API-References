---
title: FieldKeywords.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldKeywords.text property. Gets or sets the text of the keywords."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldkeywords/text/
---

## FieldKeywords.text property

Gets or sets the text of the keywords.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows to insert a KEYWORDS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add some keywords, also referred to as "tags" in File Explorer.
doc.built_in_document_properties.keywords = "Keyword1, Keyword2"

# The KEYWORDS field displays the value of this property.
field = builder.insert_field(aw.fields.FieldType.FIELD_KEYWORD, True).as_field_keywords()
field.update()

self.assertEqual(" KEYWORDS ", field.get_field_code())
self.assertEqual("Keyword1, Keyword2", field.result)

# Setting a value for the field's "text" property,
# and then updating the field will also overwrite the corresponding built-in property with the new value.
field.text = "OverridingKeyword"
field.update()

self.assertEqual(" KEYWORDS  OverridingKeyword", field.get_field_code())
self.assertEqual("OverridingKeyword", field.result)
self.assertEqual("OverridingKeyword", doc.built_in_document_properties.keywords)

doc.save(ARTIFACTS_DIR + "Field.field_keywords.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldKeywords](../)

