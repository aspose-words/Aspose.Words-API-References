---
title: PdfZoomBehavior enumeration
linktitle: PdfZoomBehavior enumeration
articleTitle: PdfZoomBehavior enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfZoomBehavior enumeration. Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer."
type: docs
weight: 770
url: /zh/python-net/aspose.words.saving/pdfzoombehavior/
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
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
# 将 "ZoomBehavior" 属性设置为 "PdfZoomBehavior.ZoomFactor" 以使 PDF 阅读器
# 在打开文档时应用基于百分比的缩放因子。
# 将 "ZoomFactor" 属性设置为 "25"，使缩放因子的值为 25%。
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# 当我们使用如 Adobe Acrobat 的阅读器打开此文档时，会看到文档被缩放至实际大小的 1/4。
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

