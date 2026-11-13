---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /es/python-net/aspose.words.saving/pssaveoptions/save_format/
---

## PsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PS](../../../aspose.words/saveformat/#PS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Cree un objeto "PsSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a PostScript.
# Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
# en el documento Postscript de salida de manera que nos ayude a crear un folleto a partir de él.
# Establezca la propiedad "UseBookFoldPrintingSettings" a "false" para guardar el documento normalmente.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# Si estamos renderizando el documento como folleto, debemos establecer "MultiplePages"
# propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Una vez que imprimamos este documento por ambas caras de las páginas, podemos doblar todas las páginas por la mitad de una sola vez,
# y el contenido se alineará de manera que cree un folleto.
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

