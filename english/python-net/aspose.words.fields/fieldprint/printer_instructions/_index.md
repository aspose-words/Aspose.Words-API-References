---
title: FieldPrint.printer_instructions property
linktitle: printer_instructions property
articleTitle: printer_instructions property
second_title: Aspose.Words for Python
description: "FieldPrint.printer_instructions property. Gets or sets the printer-specific control code characters or PostScript instructions."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldprint/printer_instructions/
---

## FieldPrint.printer_instructions property

Gets or sets the printer-specific control code characters or PostScript instructions.


### Examples

Shows to insert a PRINT field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("My paragraph")

# The PRINT field can send instructions to the printer.
field = builder.insert_field(aw.fields.FieldType.FIELD_PRINT, True).as_field_print()

# Set the area for the printer to perform instructions over.
# In this case, it will be the paragraph that contains our PRINT field.
field.post_script_group = "para"

# When we use a printer that supports PostScript to print our document,
# this command will turn the entire area that we specified in "post_script_group" white.
field.printer_instructions = "erasepage"

self.assertEqual(" PRINT  erasepage \\p para", field.get_field_code())

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_print.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

