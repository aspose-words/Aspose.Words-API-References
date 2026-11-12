---
title: FieldPrint.printer_instructions property
linktitle: printer_instructions property
articleTitle: printer_instructions property
second_title: Aspose.Words for Python
description: "FieldPrint.printer_instructions property. Gets or sets the printer-specific control code characters or PostScript instructions."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/fieldprint/printer_instructions/
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
# Поле PRINT может отправлять инструкции на принтер.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# Установите область, в которой принтер будет выполнять инструкции.
# В этом случае это будет абзац, содержащий наше поле PRINT.
field.post_script_group = 'para'
# Когда мы используем принтер, поддерживающий PostScript, для печати нашего документа,
# эта команда сделает полностью белой область, которую мы указали в "field.PostScriptGroup".
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

