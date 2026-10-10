---
title: FieldBarcode.postal_address property
linktitle: postal_address property
articleTitle: postal_address property
second_title: Aspose.Words for Python
description: "FieldBarcode.postal_address property. Gets or sets the postal address used for generating a barcode or the name of the bookmark that refers to it."
type: docs
weight: 50
url: /zh/python-net/aspose.words.fields/fieldbarcode/postal_address/
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

