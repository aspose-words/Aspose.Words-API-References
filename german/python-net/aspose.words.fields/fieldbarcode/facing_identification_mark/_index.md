---
title: FieldBarcode.facing_identification_mark property
linktitle: facing_identification_mark property
articleTitle: facing_identification_mark property
second_title: Aspose.Words for Python
description: "FieldBarcode.facing_identification_mark property. Gets or sets the type of a Facing Identification Mark (FIM) to insert."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldbarcode/facing_identification_mark/
---

## FieldBarcode.facing_identification_mark property

Gets or sets the type of a Facing Identification Mark (FIM) to insert.


```python
@property
def facing_identification_mark(self) -> str:
    ...

@facing_identification_mark.setter
def facing_identification_mark(self, value: str):
    ...

```

### Examples

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln()
# Im Folgenden werden zwei Möglichkeiten gezeigt, BARCODE‑Felder zu verwenden, um benutzerdefinierte Werte als Strichcode darzustellen.
# 1 -  Speichern Sie den Wert, den der Strichcode in der PostalAddress‑Eigenschaft anzeigen soll:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
# Dieser Wert muss eine gültige Postleitzahl sein.
field.postal_address = '96801'
field.is_us_postal_address = True
field.facing_identification_mark = 'C'
self.assertEqual(' BARCODE  96801 \\u \\f C', field.get_field_code())
builder.insert_break(aw.BreakType.LINE_BREAK)
# 2 -  Verweisen Sie auf ein Lesezeichen, das den Wert speichert, den dieser Strichcode anzeigen soll:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
field.postal_address = 'BarcodeBookmark'
field.is_bookmark = True
self.assertEqual(' BARCODE  BarcodeBookmark \\b', field.get_field_code())
# Das Lesezeichen, auf das das BARCODE‑Feld in seiner PostalAddress‑Eigenschaft verweist
# darf nichts außer der gültigen Postleitzahl enthalten.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('BarcodeBookmark')
builder.writeln('968877')
builder.end_bookmark('BarcodeBookmark')
doc.save(file_name=ARTIFACTS_DIR + 'Field.BARCODE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

