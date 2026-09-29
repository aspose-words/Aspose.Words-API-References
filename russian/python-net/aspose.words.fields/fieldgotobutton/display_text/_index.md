---
title: FieldGoToButton.display_text property
linktitle: display_text property
articleTitle: display_text property
second_title: Aspose.Words for Python
description: "FieldGoToButton.display_text property. Gets or sets the text of the button that appears in the document, such that it can be selected to activate the jump."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldgotobutton/display_text/
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
# Добавьте поле GOTOBUTTON. Когда мы дважды щёлкнем это поле в Microsoft Word,
# оно переместит текстовый курсор к закладке, имя которой указывает свойство Location.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_GO_TO_BUTTON, update_field=True).as_field_go_to_button()
field.display_text = 'My Button'
field.location = 'MyBookmark'
self.assertEqual(' GOTOBUTTON  MyBookmark My Button', field.get_field_code())
# Вставьте действительную закладку, на которую будет ссылаться поле.
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

