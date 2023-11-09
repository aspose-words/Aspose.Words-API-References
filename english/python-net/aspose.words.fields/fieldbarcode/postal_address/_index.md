---
title: FieldBarcode.postal_address property
linktitle: postal_address property
articleTitle: postal_address property
second_title: Aspose.Words for Python
description: "FieldBarcode.postal_address property. Gets or sets the postal address used for generating a barcode or the name of the bookmark that refers to it."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldbarcode/postal_address/
---

## FieldBarcode.postal_address property

Gets or sets the postal address used for generating a barcode or the name of the bookmark that refers to it.


```python
@property
def postal_address(self) -> str:
    ...

@postal_address.setter
def postal_address(self, value: str):
    ...

```

### Examples

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln()

# Below are two ways of using BARCODE fields to display custom values as barcodes.
# 1 -  Store the value that the barcode will display in the postal_address property:
field = builder.insert_field(aw.fields.FieldType.FIELD_BARCODE, True).as_field_barcode()

# This value needs to be a valid ZIP code.
field.postal_address = "96801"
field.is_us_postal_address = True
field.facing_identification_mark = "C"

self.assertEqual(" BARCODE  96801 \\u \\f C", field.get_field_code())

builder.insert_break(aw.BreakType.LINE_BREAK)

# 2 -  Reference a bookmark that stores the value that this barcode will display:
field = builder.insert_field(aw.fields.FieldType.FIELD_BARCODE, True).as_field_barcode()
field.postal_address = "BarcodeBookmark"
field.is_bookmark = True

self.assertEqual(" BARCODE  BarcodeBookmark \\b", field.get_field_code())

# The bookmark that the BARCODE field references in its "postal_address" property
# need to contain nothing besides the valid ZIP code.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark("BarcodeBookmark")
builder.writeln("968877")
builder.end_bookmark("BarcodeBookmark")

doc.save(ARTIFACTS_DIR + "Field.field_barcode.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

