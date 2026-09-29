---
title: FieldPrint.post_script_group property
linktitle: post_script_group property
articleTitle: post_script_group property
second_title: Aspose.Words for Python
description: "FieldPrint.post_script_group property. Gets or sets the drawing rectangle that the PostScript instructions operate on."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldprint/post_script_group/
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
# PRINT-fältet kan skicka instruktioner till skrivaren.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# Ange området för skrivaren att utföra instruktioner över.
# I det här fallet kommer det att vara paragrafen som innehåller vårt PRINT-fält.
field.post_script_group = 'para'
# När vi använder en skrivare som stöder PostScript för att skriva ut vårt dokument,
# kommer detta kommando att göra hela området som vi specificerade i "field.PostScriptGroup" vitt.
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

