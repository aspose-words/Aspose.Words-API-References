---
title: PdfSaveOptions.text_compression property
linktitle: text_compression property
articleTitle: text_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.text_compression property. Specifies compression type to be used for all textual content in the document."
type: docs
weight: 330
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/text_compression/
---

## PdfSaveOptions.text_compression property

Specifies compression type to be used for all textual content in the document.


```python
@property
def text_compression(self) -> aspose.words.saving.PdfTextCompression:
    ...

@text_compression.setter
def text_compression(self, value: aspose.words.saving.PdfTextCompression):
    ...

```

### Remarks

Default is [PdfTextCompression.FLATE](../../pdftextcompression/#FLATE).

Significantly increases output size when saving a document without compression.




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

