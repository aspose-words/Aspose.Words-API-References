---
title: FieldKeywords.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldKeywords.text property. Gets or sets the text of the keywords."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldkeywords/text/
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
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie einige Schlüsselwörter hinzu, die in File Explorer auch als "Tags" bezeichnet werden.
doc.built_in_document_properties.keywords = 'Keyword1, Keyword2'
# Das KEYWORDS-Feld zeigt den Wert dieser Eigenschaft an.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_KEYWORD, update_field=True).as_field_keywords()
field.update()
self.assertEqual(' KEYWORDS ', field.get_field_code())
self.assertEqual('Keyword1, Keyword2', field.result)
# Festlegen eines Werts für die Text‑Eigenschaft des Feldes,
# und das anschließende Aktualisieren des Feldes überschreibt außerdem die entsprechende integrierte Eigenschaft mit dem neuen Wert.
field.text = 'OverridingKeyword'
field.update()
self.assertEqual(' KEYWORDS  OverridingKeyword', field.get_field_code())
self.assertEqual('OverridingKeyword', field.result)
self.assertEqual('OverridingKeyword', doc.built_in_document_properties.keywords)
doc.save(file_name=ARTIFACTS_DIR + 'Field.KEYWORDS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldKeywords](../)

