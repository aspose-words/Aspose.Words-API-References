---
title: FieldBarcode.is_us_postal_address property
linktitle: is_us_postal_address property
articleTitle: is_us_postal_address property
second_title: Aspose.Words for Python
description: "FieldBarcode.is_us_postal_address property. Gets or sets whether [FieldBarcode.postal_address](../postal_address/) is a U.S"
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldbarcode/is_us_postal_address/
---

## FieldBarcode.is_us_postal_address property

Gets or sets whether [FieldBarcode.postal_address](../postal_address/) is a U.S. postal address.



```python
@property
def is_us_postal_address(self) -> bool:
    ...

@is_us_postal_address.setter
def is_us_postal_address(self, value: bool):
    ...

```

### Examples

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln()
# فيما يلي طريقتان لاستخدام حقول BARCODE لعرض قيم مخصصة كرموز شريطية.
# 1 -  خزن القيمة التي سيعرضها الرمز الشريطي في خاصية PostalAddress:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
# يجب أن تكون هذه القيمة رمز ZIP صالح.
field.postal_address = '96801'
field.is_us_postal_address = True
field.facing_identification_mark = 'C'
self.assertEqual(' BARCODE  96801 \\u \\f C', field.get_field_code())
builder.insert_break(aw.BreakType.LINE_BREAK)
# 2 -  ارجع إلى علامة مرجعية تخزن القيمة التي سيعرضها هذا الرمز الشريطي:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
field.postal_address = 'BarcodeBookmark'
field.is_bookmark = True
self.assertEqual(' BARCODE  BarcodeBookmark \\b', field.get_field_code())
# العلامة المرجعية التي يشير إليها حقل BARCODE في خاصية PostalAddress الخاصة به
# يجب أن تحتوي فقط على رمز ZIP صالح ولا شيء آخر.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('BarcodeBookmark')
builder.writeln('968877')
builder.end_bookmark('BarcodeBookmark')
doc.save(file_name=ARTIFACTS_DIR + 'Field.BARCODE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

