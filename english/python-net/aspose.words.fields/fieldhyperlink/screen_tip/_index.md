---
title: FieldHyperlink.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "FieldHyperlink.screen_tip property. Gets or sets the ScreenTip text for the hyperlink."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldhyperlink/screen_tip/
---

## FieldHyperlink.screen_tip property

Gets or sets the ScreenTip text for the hyperlink.


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

