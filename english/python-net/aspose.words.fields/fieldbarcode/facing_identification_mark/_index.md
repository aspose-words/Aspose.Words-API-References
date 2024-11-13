---
title: FieldBarcode.facing_identification_mark property
linktitle: facing_identification_mark property
articleTitle: facing_identification_mark property
second_title: Aspose.Words for Python
description: "FieldBarcode.facing_identification_mark property. Gets or sets the type of a Facing Identification Mark (FIM) to insert."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldbarcode/facing_identification_mark/
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
# Below are two ways of using BARCODE fields to display custom values as barcodes.
# 1 -  Store the value that the barcode will display in the PostalAddress property:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
# This value needs to be a valid ZIP code.
field.postal_address = '96801'
field.is_us_postal_address = True
field.facing_identification_mark = 'C'
self.assertEqual(' BARCODE  96801 \\u \\f C', field.get_field_code())
builder.insert_break(aw.BreakType.LINE_BREAK)
# 2 -  Reference a bookmark that stores the value that this barcode will display:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
field.postal_address = 'BarcodeBookmark'
field.is_bookmark = True
self.assertEqual(' BARCODE  BarcodeBookmark \\b', field.get_field_code())
# The bookmark that the BARCODE field references in its PostalAddress property
# need to contain nothing besides the valid ZIP code.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('BarcodeBookmark')
builder.writeln('968877')
builder.end_bookmark('BarcodeBookmark')
doc.save(file_name=ARTIFACTS_DIR + 'Field.BARCODE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

