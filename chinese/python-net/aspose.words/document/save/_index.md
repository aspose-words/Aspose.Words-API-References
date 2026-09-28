---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 740
url: /zh/python-net/aspose.words/document/save/
---

## save(file_name) {#str}

Saves the document to a file. Automatically determines the save format from the extension.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

### Returns

Additional information that you can optionally use.


## save(file_name, save_format) {#str_saveformat}

Saves the document to a file in the specified format.


```python
def save(self, file_name: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| save_format | [SaveFormat](../../saveformat/) | The format in which to save the document. |

### Returns

Additional information that you can optionally use.


## save(file_name, save_options) {#str_saveoptions}

Saves the document to a file using the specified save options.


```python
def save(self, file_name: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the document is saved. Can be ``None``. |

### Returns

Additional information that you can optionally use.


## save(stream, save_format) {#bytesio_saveformat}

Saves the document to a stream using the specified format.


```python
def save(self, stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream where to save the document. |
| save_format | [SaveFormat](../../saveformat/) | The format in which to save the document. |

### Returns

Additional information that you can optionally use.


## save(stream, save_options) {#bytesio_saveoptions}

Saves the document to a stream using the specified save options.


```python
def save(self, stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream where to save the document. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the document is saved. Can be ``None``. If this is ``None``, the document will be saved in the binary DOC format. |

### Returns

Additional information that you can optionally use.


## Examples

Shows how to open a document and convert it to .PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Document.ConvertToPdf.pdf')
```

Shows how to convert a PDF to a .docx.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
# 加载我们刚刚保存的 PDF 文档，并将其转换为 .docx。
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.docx')
```

Shows how to convert from DOCX to HTML format.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Document.ConvertToHtml.html', save_format=aw.SaveFormat.HTML)
```

Shows how to improve the quality of a rendered document with SaveOptions.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 60
builder.writeln('Some text.')
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.Default.jpg', save_options=options)
options.use_anti_aliasing = True
options.use_high_quality_rendering = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.HighQuality.jpg', save_options=options)
```

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# 创建一个 "ImageSaveOptions" 对象，以便我们传递给文档的 "Save" 方法
# 以修改该方法将文档渲染为图像的方式。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# 将 "PageSet" 设置为 "1" 以选择第二页，通过
# 从零基索引开始渲染文档。
options.page_set = aw.saving.PageSet(page=1)
# 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
# 此图像将包含从第二页开始的单页，
# 这将仅是原始文档的第二页。
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 创建一个 "ImageSaveOptions" 对象，以便我们传递给文档的 "Save" 方法
# 以修改该方法将文档渲染为图像的方式。
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# 将 "JpegQuality" 属性设置为 "10"，以在渲染文档时使用更强的压缩。
# 这将减小文档的文件大小，但图像会出现更明显的压缩伪影。
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# 将 "JpegQuality" 属性设置为 "100"，以在渲染文档时使用较弱的压缩。
# 这将提升图像质量，但会导致文件大小增加。
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# 创建一个 "ImageSaveOptions" 对象，以便我们传递给文档的 "save" 方法
# 以修改该方法将文档渲染为图像的方式。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # 将 "page_set" 属性设置为起始页的页码，从
    # 开始渲染文档的页面。
    options.page_set = aw.saving.PageSet(i)
    options.vertical_resolution = 600
    options.horizontal_resolution = 600
    options.image_size = aspose.pydrawing.Size(2325, 5325)
    doc.save(ARTIFACTS_DIR + f'ImageSaveOptions.page_by_page.{i + 1}.tiff', options)
```

Shows how to convert a PDF to a .docx and customize the saving process with a SaveOptions object.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
# 加载我们刚刚保存的 PDF 文档，并将其转换为 .docx。
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
# 设置 "password" 属性，以使用密码加密已保存的文档。
save_options.password = 'MyPassword'
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.docx', save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入 1 到 5 级的标题。
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 输出的 PDF 文档将包含大纲，即列出文档正文中标题的目录。
# 单击此大纲中的条目将跳转到相应标题的位置。
# 将 "HeadingsOutlineLevels" 属性设置为 "4"，以从大纲中排除所有级别高于 4 的标题。
options.outline_options.headings_outline_levels = 4
# 如果大纲条目在自身与下一个相同或更低级别的条目之间有更高级别的后续条目，
# 该条目左侧会出现一个箭头。此条目是多个此类 "sub-entries" 的 "owner"。
# 在我们的文档中，来自第 5 级标题的大纲条目是第二个第 4 级大纲条目的子条目，
# 第4和第5级标题条目是第二个第3级条目的子条目，依此类推。
# 在大纲中，我们可以点击 "owner" 条目的箭头来折叠/展开其所有子条目。
# 将 "ExpandedOutlineLevels" 属性设置为 "2"，以自动展开所有第2级及以下的标题大纲条目
# 并在打开文档时折叠所有第3级及以上的条目。
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
with io.BytesIO() as dst_stream:
    doc.save(stream=dst_stream, save_format=aw.SaveFormat.DOCX)
    # 验证流中包含该文档。
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', aw.Document(stream=dst_stream).get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

