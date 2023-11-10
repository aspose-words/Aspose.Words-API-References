---
title: FieldQuote.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldQuote.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldquote/text/
---

## FieldQuote.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a QUOTE field, which will display the value of its Text property.
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
field.text = "\"Quoted text\""

self.assertEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.get_field_code())

# Insert a QUOTE field and nest a DATE field inside it.
# DATE fields update their value to the current date every time we open the document using Microsoft Word.
# Nesting the DATE field inside the QUOTE field like this will freeze its value
# to the date when we created the document.
builder.write("\nDocument creation date: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(aw.fields.FieldType.FIELD_DATE, True)

today = datetime.now().strftime("%d/%m/%Y").lstrip('0')

self.assertEqual(" QUOTE \u0013 DATE \u0014" + today + "\u0015", field.get_field_code())

# Update all the fields to display their correct results.
doc.update_fields()

self.assertEqual("\"Quoted text\"", doc.range.fields[0].result)

doc.save(ARTIFACTS_DIR + "Field.field_quote.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldQuote](../)

