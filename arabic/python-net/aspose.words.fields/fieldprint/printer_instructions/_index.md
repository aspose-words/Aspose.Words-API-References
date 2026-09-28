---
title: FieldPrint.printer_instructions property
linktitle: printer_instructions property
articleTitle: printer_instructions property
second_title: Aspose.Words for Python
description: "FieldPrint.printer_instructions property. Gets or sets the printer-specific control code characters or PostScript instructions."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fields/fieldprint/printer_instructions/
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
# يمكن للحقل PRINT إرسال التعليمات إلى الطابعة.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# حدد المنطقة التي تنفذ الطابعة التعليمات عليها.
# في هذه الحالة، سيكون الفقرة التي تحتوي على حقل PRINT الخاص بنا.
field.post_script_group = 'para'
# عند استخدامنا لطابعة تدعم PostScript لطباعة مستندنا،
# سيحول هذا الأمر المنطقة بالكامل التي حددناها في "field.PostScriptGroup" إلى اللون الأبيض.
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

