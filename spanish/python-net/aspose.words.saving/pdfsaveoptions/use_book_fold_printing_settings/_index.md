---
title: PdfSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 340
url: /es/python-net/aspose.words.saving/pdfsaveoptions/use_book_fold_printing_settings/
---

## PdfSaveOptions.use_book_fold_printing_settings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/).



```python
@property
def use_book_fold_printing_settings(self) -> bool:
    ...

@use_book_fold_printing_settings.setter
def use_book_fold_printing_settings(self, value: bool):
    ...

```

### Remarks

If this option is specified, [FixedPageSaveOptions.page_set](../../fixedpagesaveoptions/page_set/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





### Examples

Shows how to save a document to the PDF format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
# en el PDF de salida de manera que nos ayude a usarlo para crear un folleto.
# Establezca la propiedad "UseBookFoldPrintingSettings" en "false" para renderizar el PDF normalmente.
options.use_book_fold_printing_settings = render_text_as_bookfold
# Si estamos renderizando el documento como folleto, debemos establecer "MultiplePages"
# propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if render_text_as_bookfold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Una vez que imprimamos este documento por ambas caras de las páginas, podemos doblar todas las páginas por la mitad de una sola vez,
# y el contenido se alineará de manera que cree un folleto.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.SaveAsPdfBookFold.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

