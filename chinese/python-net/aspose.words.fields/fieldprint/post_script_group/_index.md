---
title: FieldPrint.post_script_group property
linktitle: post_script_group property
articleTitle: post_script_group property
second_title: Aspose.Words for Python
description: "FieldPrint.post_script_group property. Gets or sets the drawing rectangle that the PostScript instructions operate on."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldprint/post_script_group/
---

## FieldPrint.post_script_group property

Gets or sets the drawing rectangle that the PostScript instructions operate on.


```python
@property
def post_script_group(self) -> str:
    ...

@post_script_group.setter
def post_script_group(self, value: str):
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

