---
title: PdfSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "PdfSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 390
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```python
def clone(self):
    ...
```

### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga text med PAGE- och NUMPAGES-fält. Dessa fält visar inte det korrekta värdet i realtid.
# Vi kommer att behöva uppdatera dem manuellt med uppdateringsmetoder såsom "Field.Update()", och "Document.UpdateFields()"
# varje gång vi behöver att de visar korrekta värden.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "UpdateFields" till "false" för att inte uppdatera alla fält i ett dokument precis före en sparoperation.
# Detta är det föredragna alternativet om vi vet att alla våra fält kommer att vara uppdaterade innan sparning.
# Ställ in egenskapen "UpdateFields" till "true" för att iterera genom hela dokumentet
# fält och uppdatera dem innan vi sparar det som en PDF. Detta säkerställer att alla fält kommer att visa
# de mest exakta värdena i PDF:en.
options.update_fields = update_fields
# Vi kan klona PdfSaveOptions-objekt.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

