---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /de/python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Text mit den Feldern PAGE und NUMPAGES ein. Diese Felder zeigen den korrekten Wert nicht in Echtzeit an.
# Wir müssen sie manuell aktualisieren, indem wir Aktualisierungsmethoden wie "Field.Update()" und "Document.UpdateFields()" verwenden.
# jedes Mal, wenn wir benötigen, dass sie genaue Werte anzeigen.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "UpdateFields" auf "false", um nicht alle Felder in einem Dokument unmittelbar vor einem Speichervorgang zu aktualisieren.
# Dies ist die bevorzugte Option, wenn wir wissen, dass alle unsere Felder vor dem Speichern aktuell sind.
# Setzen Sie die Eigenschaft "UpdateFields" auf "true", um durch das gesamte Dokument zu iterieren
# Felder und aktualisieren sie, bevor wir es als PDF speichern. Dadurch wird sichergestellt, dass alle Felder anzeigen
# die genauesten Werte im PDF.
options.update_fields = update_fields
# Wir können PdfSaveOptions-Objekte klonen.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

