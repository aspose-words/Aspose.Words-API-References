---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 770
url: /ru/python-net/aspose.words.saving/pdfzoombehavior/
---

## PdfZoomBehavior enumeration

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.


### Members

| Name | Description |
| --- | --- |
| NONE | How the document is displayed is left to the PDF viewer. Usually the viewer displays the document to fit page width. |
| ZOOM_FACTOR | Displays the page using the specified zoom factor. |
| FIT_PAGE | Displays the page so it visible entirely. |
| FIT_WIDTH | Fits the width of the page. |
| FIT_HEIGHT | Fits the height of the page. |
| FIT_BOX | Fits the bounding box (rectangle containing all visible elements on the page). |

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

* module [aspose.words.saving](../)

