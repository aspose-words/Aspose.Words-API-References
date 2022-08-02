---
title: location property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of a bookmark, a page number, or some other item to jump to."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldgotobutton/location/
---

## FieldGoToButton.location property

Gets or sets the name of a bookmark, a page number, or some other item to jump to.


### Examples

Shows to insert a GOTOBUTTON field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add a GOTOBUTTON field. When we double-click this field in Microsoft Word,
# it will take the text cursor to the bookmark whose name the Location property references.
field = builder.insert_field(aw.fields.FieldType.FIELD_GO_TO_BUTTON, True).as_field_go_to_button()
field.display_text = "My Button"
field.location = "MyBookmark"

self.assertEqual(" GOTOBUTTON  MyBookmark My Button", field.get_field_code())

# Insert a valid bookmark for the field to reference.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark(field.location)
builder.writeln("Bookmark text contents.")
builder.end_bookmark(field.location)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_go_to_button.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldGoToButton](../)

