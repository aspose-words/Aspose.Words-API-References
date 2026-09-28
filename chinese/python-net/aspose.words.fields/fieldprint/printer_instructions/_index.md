---
title: FieldPrint.printer_instructions property
linktitle: printer_instructions property
articleTitle: printer_instructions property
second_title: Aspose.Words for Python
description: "FieldPrint.printer_instructions property. Gets or sets the printer-specific control code characters or PostScript instructions."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldprint/printer_instructions/
---

## FieldPrint.printer_instructions property

Gets or sets the printer-specific control code characters or PostScript instructions.


```python
@property
def printer_instructions(self) -> str:
    ...

@printer_instructions.setter
def printer_instructions(self, value: str):
    ...

```

### Examples

Shows to insert a PRINT field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('My paragraph')
# PRINT 字段可以向打印机发送指令。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# 设置打印机执行指令的区域。
# 在这种情况下，它将是包含我们 PRINT 字段的段落。
field.post_script_group = 'para'
# 当我们使用支持 PostScript 的打印机来打印文档时，
# 此命令会将我们在 "field.PostScriptGroup" 中指定的整个区域变为白色。
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

