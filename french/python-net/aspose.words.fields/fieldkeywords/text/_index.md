---
title: FieldKeywords.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldKeywords.text property. Gets or sets the text of the keywords."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldkeywords/text/
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
# Ajoutez quelques mots-clés, également appelés "tags" dans l'Explorateur de fichiers.
doc.built_in_document_properties.keywords = 'Keyword1, Keyword2'
# Le champ KEYWORDS affiche la valeur de cette propriété.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_KEYWORD, update_field=True).as_field_keywords()
field.update()
self.assertEqual(' KEYWORDS ', field.get_field_code())
self.assertEqual('Keyword1, Keyword2', field.result)
# Définir une valeur pour la propriété Text du champ,
# et ensuite mettre à jour le champ écrasera également la propriété intégrée correspondante avec la nouvelle valeur.
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

