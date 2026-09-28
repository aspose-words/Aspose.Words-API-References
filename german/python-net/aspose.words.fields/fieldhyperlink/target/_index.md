---
title: FieldHyperlink.target property
linktitle: target property
articleTitle: target property
second_title: Aspose.Words for Python
description: "FieldHyperlink.target property. Gets or sets the target to which the link should be redirected."
type: docs
weight: 70
url: /de/python-net/aspose.words.fields/fieldhyperlink/target/
---

## FieldHyperlink.target property

Gets or sets the target to which the link should be redirected.


```python
@property
def target(self) -> str:
    ...

@target.setter
def target(self, value: str):
    ...

```

### Examples

Shows how to use HYPERLINK fields to link to documents in the local file system.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_HYPERLINK, update_field=True).as_field_hyperlink()
# Wenn wir dieses HYPERLINK-Feld in Microsoft Word anklicken,
# wird das verknüpfte Dokument geöffnet und anschließend der Cursor an der angegebenen Lesezeichenposition platziert.
field.address = MY_DIR + 'Bookmarks.docx'
field.sub_address = 'MyBookmark3'
field.screen_tip = 'Open ' + field.address + ' on bookmark ' + field.sub_address + ' in a new window'
builder.writeln()
# Wenn wir dieses HYPERLINK-Feld in Microsoft Word anklicken,
# es wird das verknüpfte Dokument öffnen und automatisch zum angegebenen iframe scrollen.
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

