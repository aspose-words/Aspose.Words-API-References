---
title: PdfTextCompression enumeration
linktitle: PdfTextCompression enumeration
articleTitle: PdfTextCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfTextCompression enumeration. Specifies a type of compression applied to all content in the PDF file except images."
type: docs
weight: 760
url: /zh/python-net/aspose.words.saving/pdftextcompression/
---

## PdfTextCompression enumeration

Specifies a type of compression applied to all content in the PDF file except images.


### Members

| Name | Description |
| --- | --- |
| NONE | No compression. |
| FLATE | Flate (ZIP) compression. |

### Examples

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 100:
    builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    i += 1
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 将 "TextCompression" 属性设置为 "PdfTextCompression.None"，以不应用任何
# 在将文档保存为 PDF 时不对文本进行任何压缩。
# 将 "TextCompression" 属性设置为 "PdfTextCompression.Flate"，以应用 ZIP 压缩
# 在将文档保存为 PDF 时对文本进行压缩。文档越大，影响越大。
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

