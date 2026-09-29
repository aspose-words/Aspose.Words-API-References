---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words.saving/xpssaveoptions/__init__/
---

## XpsSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) format.



```python
def __init__(self):
    ...
```

## XpsSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) or [SaveFormat.OPEN_XPS](../../../aspose.words/saveformat/#OPEN_XPS) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Establezca la propiedad "UseBookFoldPrintingSettings" a "true" para organizar el contenido
# en el XPS de salida de una manera que nos ayuda a usarlo para crear un folleto.
# Establezca la propiedad "UseBookFoldPrintingSettings" en "false" para renderizar el XPS normalmente.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Si estamos renderizando el documento como folleto, debemos establecer "MultiplePages"
# propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Una vez que imprimimos este documento, podemos convertirlo en un folleto apilando las páginas
# para que salgan de la impresora y se plieguen por la mitad.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

