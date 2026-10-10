---
title: FieldPrint.post_script_group property
linktitle: post_script_group property
articleTitle: post_script_group property
second_title: Aspose.Words for Python
description: "FieldPrint.post_script_group property. Gets or sets the drawing rectangle that the PostScript instructions operate on."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldprint/post_script_group/
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
# Das PRINT-Feld kann Anweisungen an den Drucker senden.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# Legen Sie den Bereich fest, in dem der Drucker Anweisungen ausführen soll.
# In diesem Fall ist es der Absatz, der unser PRINT-Feld enthält.
field.post_script_group = 'para'
# Wenn wir einen Drucker verwenden, der PostScript unterstützt, um unser Dokument zu drucken,
# wird dieser Befehl den gesamten Bereich, den wir in \"field.PostScriptGroup\" angegeben haben, weiß färben.
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

