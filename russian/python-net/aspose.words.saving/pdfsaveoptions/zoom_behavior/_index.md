---
title: PdfSaveOptions.zoom_behavior property
linktitle: zoom_behavior property
articleTitle: zoom_behavior property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_behavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 370
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/zoom_behavior/
---

## PdfSaveOptions.zoom_behavior property

Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.


```python
@property
def zoom_behavior(self) -> aspose.words.saving.PdfZoomBehavior:
    ...

@zoom_behavior.setter
def zoom_behavior(self, value: aspose.words.saving.PdfZoomBehavior):
    ...

```

### Remarks

The default value is [PdfZoomBehavior.NONE](../../pdfzoombehavior/#NONE), i.e. no fit is applied.



### Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
# Установите свойство "ZoomBehavior" в значение "PdfZoomBehavior.ZoomFactor", чтобы PDF‑читалка
# применяла масштабирование на основе процента при открытии документа.
# Установите свойство "ZoomFactor" в "25", чтобы задать коэффициент масштабирования 25%.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# Когда мы открываем этот документ с помощью читателя, например Adobe Acrobat, мы увидим документ, масштабированный до 1/4 его реального размера.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

