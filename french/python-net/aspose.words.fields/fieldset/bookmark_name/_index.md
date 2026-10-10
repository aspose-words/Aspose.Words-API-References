---
title: FieldSet.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSet.bookmark_name property. Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldset/bookmark_name/
---

## FieldSet.bookmark_name property

Gets or sets the name of the bookmark.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Nommer le texte marqué d'un signet avec un champ SET.
# Ce champ fait référence au "bookmark" non pas à une structure de signet qui apparaît dans le texte, mais à une variable nommée.
field_set = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SET, update_field=False).as_field_set()
field_set.bookmark_name = 'MyBookmark'
field_set.bookmark_text = 'Hello world!'
field_set.update()
self.assertEqual(' SET  MyBookmark "Hello world!"', field_set.get_field_code())
# Faites référence au signet par son nom dans un champ REF et affichez son contenu.
field_ref = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
field_ref.bookmark_name = 'MyBookmark'
field_ref.update()
self.assertEqual(' REF  MyBookmark', field_ref.get_field_code())
self.assertEqual('Hello world!', field_ref.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.SET.REF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSet](../)

