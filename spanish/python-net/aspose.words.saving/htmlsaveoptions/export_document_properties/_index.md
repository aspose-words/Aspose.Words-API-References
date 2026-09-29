---
title: HtmlSaveOptions.export_document_properties property
linktitle: export_document_properties property
articleTitle: export_document_properties property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_document_properties property. Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB"
type: docs
weight: 120
url: /es/python-net/aspose.words.saving/htmlsaveoptions/export_document_properties/
---

## HtmlSaveOptions.export_document_properties property

Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB.
Default value is ``False``.



```python
@property
def export_document_properties(self) -> bool:
    ...

@export_document_properties.setter
def export_document_properties(self, value: bool):
    ...

```

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Utilice un objeto SaveOptions para especificar la codificación de un documento que vamos a guardar.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Por defecto, un documento .epub de salida tendrá todo su contenido en una única parte HTML.
# Un criterio de división nos permite segmentar el documento en varias partes HTML.
# Estableceremos los criterios para dividir el documento en párrafos de encabezado.
# Esto es útil para lectores que no pueden leer archivos HTML mayores que un tamaño específico.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Especifique que queremos exportar las propiedades del documento.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

