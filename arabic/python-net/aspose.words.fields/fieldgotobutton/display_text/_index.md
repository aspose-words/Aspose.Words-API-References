---
title: FieldGoToButton.display_text property
linktitle: display_text property
articleTitle: display_text property
second_title: Aspose.Words for Python
description: "FieldGoToButton.display_text property. Gets or sets the text of the button that appears in the document, such that it can be selected to activate the jump."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldgotobutton/display_text/
---

## FieldGoToButton.display_text property

Gets or sets the text of the "button" that appears in the document, such that it can be selected to activate the jump.


```python
@property
def display_text(self) -> str:
    ...

@display_text.setter
def display_text(self, value: str):
    ...

```

### Examples

Shows to insert a GOTOBUTTON field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أضف حقل GOTOBUTTON. عندما نقوم بالنقر المزدوج على هذا الحقل في Microsoft Word،
# سوف ينقل مؤشر النص إلى العلامة المرجعية التي يشير إليها خاصية Location.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_GO_TO_BUTTON, update_field=True).as_field_go_to_button()
field.display_text = 'My Button'
field.location = 'MyBookmark'
self.assertEqual(' GOTOBUTTON  MyBookmark My Button', field.get_field_code())
# أدرج علامة مرجعية صالحة ليشير إليها الحقل.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark(field.location)
builder.writeln('Bookmark text contents.')
builder.end_bookmark(field.location)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.GOTOBUTTON.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldGoToButton](../)

