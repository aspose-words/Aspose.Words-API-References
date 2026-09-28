---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 740
url: /ar/python-net/aspose.words/document/save/
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
# حمّل مستند PDF الذي حفظناه للتو، وحوّله إلى .docx.
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
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# عيّن "PageSet" إلى "1" لاختيار الصفحة الثانية عبر
# الفهرس الصفري للبدء في تحويل المستند من.
options.page_set = aw.saving.PageSet(page=1)
# عند حفظ المستند بتنسيق JPEG، تقوم Aspose.Words بتحويل صفحة واحدة فقط.
# ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية،
# وهي ببساطة الصفحة الثانية من المستند الأصلي.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# قم بتعيين الخاصية "JpegQuality" إلى "10" لاستخدام ضغط أقوى عند عرض المستند.
# سيؤدي ذلك إلى تقليل حجم ملف المستند، لكن الصورة ستظهر عيوب ضغط أكثر وضوحًا.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# قم بتعيين الخاصية "JpegQuality" إلى "100" لاستخدام ضغط أضعف عند عرض المستند.
# سيحسن هذا جودة الصورة على حساب زيادة حجم الملف.
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
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # عيّن خاصية "page_set" إلى رقم الصفحة الأولى من
    # التي نبدأ منها في تحويل المستند.
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
# حمّل مستند PDF الذي حفظناه للتو، وحوّله إلى .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
# عيّن خاصية "password" لتشفير المستند المحفوظ بكلمة مرور.
save_options.password = 'MyPassword'
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.docx', save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج عناوين بالمستويات من 1 إلى 5.
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
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# سيحتوي مستند PDF الناتج على مخطط، وهو جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# اضبط خاصية "HeadingsOutlineLevels" إلى "4" لاستبعاد جميع العناوين التي مستوياتها فوق 4 من المخطط.
options.outline_options.headings_outline_levels = 4
# إذا كان لمدخل المخطط مدخلات لاحقة ذات مستوى أعلى بينه وبين المدخل التالي من نفس المستوى أو مستوى أدنى،
# ستظهر سهم إلى يسار المدخل. هذا المدخل هو "المالك" لعدة "مدخلات فرعية" مماثلة.
# في مستندنا، مدخلات المخطط من المستوى الخامس هي مدخلات فرعية للمدخل الثاني من المستوى الرابع في المخطط،
# الإدخالات من المستوى الرابع والخامس هي إدخالات فرعية للإدخال الثاني من المستوى الثالث، وهكذا.
# في المخطط، يمكننا النقر على السهم الخاص بإدخال "owner" لتقليص/توسيع جميع الإدخالات الفرعية الخاصة به.
# قم بتعيين الخاصية "ExpandedOutlineLevels" إلى "2" لتوسيع جميع إدخالات المخطط من المستوى 2 وما أدناه تلقائيًا
# وتقليص جميع الإدخالات من المستوى 3 وما أعلى عند فتح المستند.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
with io.BytesIO() as dst_stream:
    doc.save(stream=dst_stream, save_format=aw.SaveFormat.DOCX)
    # تحقق من أن الدفق يحتوي على المستند.
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', aw.Document(stream=dst_stream).get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

