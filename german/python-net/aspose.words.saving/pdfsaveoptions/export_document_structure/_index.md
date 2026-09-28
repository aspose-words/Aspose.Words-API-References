---
title: PdfSaveOptions.export_document_structure property
linktitle: export_document_structure property
articleTitle: export_document_structure property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_document_structure property. Gets or sets a value determining whether or not to export document structure."
type: docs
weight: 140
url: /de/python-net/aspose.words.saving/pdfsaveoptions/export_document_structure/
---

## PdfSaveOptions.export_document_structure property

Gets or sets a value determining whether or not to export document structure.


```python
@property
def export_document_structure(self) -> bool:
    ...

@export_document_structure.setter
def export_document_structure(self, value: bool):
    ...

```

### Remarks

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially
for the large documents.




### Examples

Shows how to preserve document structure elements, which can assist in programmatically interpreting our document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "ExportDocumentStructure" auf "true", um die Dokumentenstruktur, solche Tags, über das
# "Content"-Navigationsbereich von Adobe Acrobat auf Kosten einer erhöhten Dateigröße.
# Setzen Sie die Eigenschaft "ExportDocumentStructure" auf "false", um die Dokumentenstruktur nicht zu exportieren.
options.export_document_structure = export_document_structure
# Angenommen, wir exportieren die Dokumentenstruktur beim Speichern dieses Dokuments. In diesem Fall,
# können wir es mit Adobe Acrobat öffnen und Tags für Elemente wie die Überschrift finden
# und den nächsten Absatz über "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportDocumentStructure.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

