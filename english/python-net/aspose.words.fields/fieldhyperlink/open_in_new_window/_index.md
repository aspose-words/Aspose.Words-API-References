---
title: FieldHyperlink.open_in_new_window property
linktitle: open_in_new_window property
articleTitle: open_in_new_window property
second_title: Aspose.Words for Python
description: "FieldHyperlink.open_in_new_window property. Gets or sets whether to open the destination site in a new web browser window."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldhyperlink/open_in_new_window/
---

## FieldHyperlink.open_in_new_window property

Gets or sets whether to open the destination site in a new web browser window.


```python
@property
def open_in_new_window(self) -> bool:
    ...

@open_in_new_window.setter
def open_in_new_window(self, value: bool):
    ...

```

### Examples

Shows how to use HYPERLINK fields to link to documents in the local file system.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field(aw.fields.FieldType.FIELD_HYPERLINK, True).as_field_hyperlink()

# When we click this HYPERLINK field in Microsoft Word,
# it will open the linked document and then place the cursor at the specified bookmark.
field.address = MY_DIR + "Bookmarks.docx"
field.sub_address = "MyBookmark3"
field.screen_tip = "Open " + field.address + " on bookmark " + field.sub_address + " in a new window"

builder.writeln()

# When we click this HYPERLINK field in Microsoft Word,
# it will open the linked document, and automatically scroll down to the specified iframe.
field = builder.insert_field(aw.fields.FieldType.FIELD_HYPERLINK, True).as_field_hyperlink()
field.address = MY_DIR + "Iframes.html"
field.screen_tip = "Open " + field.address
field.target = "iframe_3"
field.open_in_new_window = True
field.is_image_map = False

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_hyperlink.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldHyperlink](../)

