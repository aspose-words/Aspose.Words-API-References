---
title: FieldDisplayBarcode.error_correction_level property
linktitle: error_correction_level property
articleTitle: error_correction_level property
second_title: Aspose.Words for Python
description: "FieldDisplayBarcode.error_correction_level property. Gets or sets an error correction level of QR Code"
type: docs
weight: 80
url: /python-net/aspose.words.fields/fielddisplaybarcode/error_correction_level/
---

## FieldDisplayBarcode.error_correction_level property

Gets or sets an error correction level of QR Code. Valid values are [0, 3].


```python
@property
def error_correction_level(self) -> str:
    ...

@error_correction_level.setter
def error_correction_level(self, value: str):
    ...

```

### Examples

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
field = builder.insert_field(aw.fields.FieldType.FIELD_DISPLAY_BARCODE, True).as_field_display_barcode()
# Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
# 1 -  QR code with custom colors:
field.barcode_type = 'QR'
field.barcode_value = 'ABC123'
field.background_color = '0xF8BD69'
field.foreground_color = '0xB5413B'
field.error_correction_level = '3'
field.scaling_factor = '250'
field.symbol_height = '1000'
field.symbol_rotation = '0'
self.assertEqual(' DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0', field.get_field_code())
builder.writeln()
# 2 -  EAN13 barcode, with the digits displayed below the bars:
field = builder.insert_field(aw.fields.FieldType.FIELD_DISPLAY_BARCODE, True).as_field_display_barcode()
field.barcode_type = 'EAN13'
field.barcode_value = '501234567890'
field.display_text = True
field.pos_code_style = 'CASE'
field.fix_check_digit = True
self.assertEqual(' DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x', field.get_field_code())
builder.writeln()
# 3 -  CODE39 barcode:
field = builder.insert_field(aw.fields.FieldType.FIELD_DISPLAY_BARCODE, True).as_field_display_barcode()
field.barcode_type = 'CODE39'
field.barcode_value = '12345ABCDE'
field.add_start_stop_char = True
self.assertEqual(' DISPLAYBARCODE  12345ABCDE CODE39 \\d', field.get_field_code())
builder.writeln()
# 4 -  ITF4 barcode, with a specified case code:
field = builder.insert_field(aw.fields.FieldType.FIELD_DISPLAY_BARCODE, True).as_field_display_barcode()
field.barcode_type = 'ITF14'
field.barcode_value = '09312345678907'
field.case_code_style = 'STD'
self.assertEqual(' DISPLAYBARCODE  09312345678907 ITF14 \\c STD', field.get_field_code())
doc.save(ARTIFACTS_DIR + 'Field.field_display_barcode.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldDisplayBarcode](../)

