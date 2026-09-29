---
title: FieldSet.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSet.bookmark_name property. Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldset/bookmark_name/
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
# Namnge bokmärkt text med ett SET-fält.
# Detta fält refererar till "bookmark" – inte en bokmärkesstruktur som visas i texten, utan en namngiven variabel.
field_set = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SET, update_field=False).as_field_set()
field_set.bookmark_name = 'MyBookmark'
field_set.bookmark_text = 'Hello world!'
field_set.update()
self.assertEqual(' SET  MyBookmark "Hello world!"', field_set.get_field_code())
# Referera till bokmärket med namn i ett REF-fält och visa dess innehåll.
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

