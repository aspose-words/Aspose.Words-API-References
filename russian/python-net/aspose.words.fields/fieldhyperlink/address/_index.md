---
title: FieldHyperlink.address property
linktitle: address property
articleTitle: address property
second_title: Aspose.Words for Python
description: "FieldHyperlink.address property. Gets or sets a location where this hyperlink jumps."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldhyperlink/address/
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
# Когда мы щёлкаем по этому полю HYPERLINK в Microsoft Word,
# он откроет связанный документ и затем переместит курсор к указанной закладке.
field.address = MY_DIR + 'Bookmarks.docx'
field.sub_address = 'MyBookmark3'
field.screen_tip = 'Open ' + field.address + ' on bookmark ' + field.sub_address + ' in a new window'
builder.writeln()
# Когда мы щёлкаем по этому полю HYPERLINK в Microsoft Word,
# он откроет связанный документ и автоматически прокрутит вниз до указанного iframe.
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

