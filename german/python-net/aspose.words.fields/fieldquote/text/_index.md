---
title: FieldQuote.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldQuote.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldquote/text/
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
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein QUOTE-Feld ein, das den Wert seiner Text-Eigenschaft anzeigt.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# Fügen Sie ein QUOTE-Feld ein und betten Sie ein DATE-Feld darin ein.
# DATE-Felder aktualisieren ihren Wert bei jedem Öffnen des Dokuments mit Microsoft Word auf das aktuelle Datum.
# Das Verschachteln des DATE-Feldes innerhalb des QUOTE-Feldes auf diese Weise friert seinen Wert ein
# auf das Datum, an dem wir das Dokument erstellt haben.
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# Aktualisieren Sie alle Felder, damit sie ihre korrekten Ergebnisse anzeigen.
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldQuote](../)

