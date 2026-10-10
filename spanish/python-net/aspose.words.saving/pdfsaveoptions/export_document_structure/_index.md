---
title: PdfSaveOptions.export_document_structure property
linktitle: export_document_structure property
articleTitle: export_document_structure property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_document_structure property. Gets or sets a value determining whether or not to export document structure."
type: docs
weight: 140
url: /es/python-net/aspose.words.saving/pdfsaveoptions/export_document_structure/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "ExportDocumentStructure" en "true" para que la estructura del documento, como esas etiquetas, esté disponible a través del
# panel de navegación "Content" de Adobe Acrobat a costa de un mayor tamaño de archivo.
# Establezca la propiedad "ExportDocumentStructure" en "false" para no exportar la estructura del documento.
options.export_document_structure = export_document_structure
# Supongamos que exportamos la estructura del documento al guardar este documento. En ese caso,
# podemos abrirlo con Adobe Acrobat y encontrar etiquetas para elementos como el encabezado
# y el siguiente párrafo mediante "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportDocumentStructure.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

