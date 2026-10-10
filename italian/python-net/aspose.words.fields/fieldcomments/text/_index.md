---
title: FieldComments.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldComments.text property. Gets or sets the text of the comments."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fieldcomments/text/
---

## FieldComments.text property

Gets or sets the text of the comments.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the COMMENTS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Imposta un valore per la proprietà incorporata "Comments" del documento.
doc.built_in_document_properties.comments = 'My comment.'
# Crea un campo COMMENTS per visualizzare il valore di quella proprietà incorporata.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True).as_field_comments()
field.update()
self.assertEqual(' COMMENTS ', field.get_field_code())
self.assertEqual('My comment.', field.result)
# Se assegniamo un valore alla proprietà Text del campo COMMENTS e lo aggiorniamo, il campo
# sovrascriverà il valore corrente della proprietà incorporata "Comments" con il valore della sua proprietà Text,
# e quindi visualizzerà il nuovo valore.
field.text = 'My overriding comment.'
field.update()
self.assertEqual(' COMMENTS  "My overriding comment."', field.get_field_code())
self.assertEqual('My overriding comment.', field.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMMENTS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldComments](../)

