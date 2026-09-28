---
title: FieldHyperlink.address property
linktitle: address property
articleTitle: address property
second_title: Aspose.Words for Python
description: "FieldHyperlink.address property. Gets or sets a location where this hyperlink jumps."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldhyperlink/address/
---

## FieldHyperlink.address property

Gets or sets a location where this hyperlink jumps.


```python
@property
def address(self) -> str:
    ...

@address.setter
def address(self, value: str):
    ...

```

### Examples

Shows how to use HYPERLINK fields to link to documents in the local file system.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_HYPERLINK, update_field=True).as_field_hyperlink()
# عند النقر على حقل HYPERLINK هذا في Microsoft Word،
# سيفتح المستند المرتبط ثم يضع المؤشر عند العلامة المرجعية المحددة.
field.address = MY_DIR + 'Bookmarks.docx'
field.sub_address = 'MyBookmark3'
field.screen_tip = 'Open ' + field.address + ' on bookmark ' + field.sub_address + ' in a new window'
builder.writeln()
# عند النقر على حقل HYPERLINK هذا في Microsoft Word،
# سيفتح المستند المرتبط، ويقوم تلقائيًا بالتمرير إلى iframe المحدد.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_HYPERLINK, update_field=True).as_field_hyperlink()
field.address = MY_DIR + 'Iframes.html'
field.screen_tip = 'Open ' + field.address
field.target = 'iframe_3'
field.open_in_new_window = True
field.is_image_map = False
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.HYPERLINK.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldHyperlink](../)

