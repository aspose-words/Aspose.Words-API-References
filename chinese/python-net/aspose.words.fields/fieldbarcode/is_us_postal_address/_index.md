---
title: FieldBarcode.is_us_postal_address property
linktitle: is_us_postal_address property
articleTitle: is_us_postal_address property
second_title: Aspose.Words for Python
description: "FieldBarcode.is_us_postal_address property. Gets or sets whether [FieldBarcode.postal_address](../postal_address/) is a U.S"
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldbarcode/is_us_postal_address/
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
# 下面是使用 BARCODE 字段显示自定义值为条形码的两种方法。
# 1 - 将条形码将显示的值存储在 PostalAddress 属性中：
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
# 此值需要是有效的 ZIP 代码。
field.postal_address = '96801'
field.is_us_postal_address = True
field.facing_identification_mark = 'C'
self.assertEqual(' BARCODE  96801 \\u \\f C', field.get_field_code())
builder.insert_break(aw.BreakType.LINE_BREAK)
# 2 - 引用存储此条形码将显示的值的书签：
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BARCODE, update_field=True).as_field_barcode()
field.postal_address = 'BarcodeBookmark'
field.is_bookmark = True
self.assertEqual(' BARCODE  BarcodeBookmark \\b', field.get_field_code())
# BARCODE 字段在其 PostalAddress 属性中引用的书签
# 只能包含有效的 ZIP 代码，不能有其他内容。
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('BarcodeBookmark')
builder.writeln('968877')
builder.end_bookmark('BarcodeBookmark')
doc.save(file_name=ARTIFACTS_DIR + 'Field.BARCODE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldBarcode](../)

