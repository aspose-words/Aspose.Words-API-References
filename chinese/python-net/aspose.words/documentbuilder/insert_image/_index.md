---
title: DocumentBuilder.insert_image method
linktitle: insert_image method
articleTitle: insert_image method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_image method"
type: docs
weight: 400
url: /zh/python-net/aspose.words/documentbuilder/insert_image/
---

## insert_image(file_name) {#str}

```python
def insert_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## insert_image(stream) {#bytesio}

```python
def insert_image(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO |  |

## insert_image(image_bytes) {#bytes}

```python
def insert_image(self, image_bytes: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes |  |

## insert_image(file_name, width, height) {#str_float_float}

```python
def insert_image(self, file_name: str, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| width | float |  |
| height | float |  |

## insert_image(stream, width, height) {#bytesio_float_float}

```python
def insert_image(self, stream: io.BytesIO, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO |  |
| width | float |  |
| height | float |  |

## insert_image(image_bytes, width, height) {#bytes_float_float}

```python
def insert_image(self, image_bytes: bytes, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes |  |
| width | float |  |
| height | float |  |

## insert_image(file_name, horz_pos, left, vert_pos, top, width, height, wrap_type) {#str_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

```python
def insert_image(self, file_name: str, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

## insert_image(stream, horz_pos, left, vert_pos, top, width, height, wrap_type) {#bytesio_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

```python
def insert_image(self, stream: io.BytesIO, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

## insert_image(image_bytes, horz_pos, left, vert_pos, top, width, height, wrap_type) {#bytes_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

```python
def insert_image(self, image_bytes: bytes, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

## Examples

Shows how to insert an image from the local file system into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 以下是从本地系统文件名插入图像的三种方式。
# 1 - 基于图像原始尺寸的默认大小的内联形状：
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 2 - 自定义尺寸的内联形状：
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png', width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 3 - 自定义尺寸的浮动形状：
builder.insert_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertImageFromFilename.docx')
```

Shows how to determine which image will be inserted.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Scalable Vector Graphics.svg')
# Aspose.Words 将 SVG 图像插入文档为 PNG，使用 svgBlip 扩展名
# 其中包含原始矢量 SVG 图像表示。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx')
# Aspose.Words 将 SVG 图像插入文档为 PNG，正如 Microsoft Word 对旧格式的处理方式。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.Svg.doc')
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
# Aspose.Words 将 SVG 图像插入文档为 EMF 元文件，以保持图像的矢量表示。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.Emf.docx')
```

Shows how to insert gif image to the document.

```python
builder = aw.DocumentBuilder()
# 我们可以使用路径或字节数组插入 gif 图像。
# 仅当 DocumentBuilder 优化到 Word 2010 或更高版本时才有效。
# 注意，访问图像字节会导致 Gif 转换为 Png。
gif_image = builder.insert_image(file_name=IMAGE_DIR + 'Graphics Interchange Format.gif')
gif_image = builder.insert_image(image_bytes=system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Graphics Interchange Format.gif'))
builder.document.save(file_name=ARTIFACTS_DIR + 'InsertGif.docx')
```

Shows how to insert a shape with an image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 以下是文档生成器的 "InsertShape" 方法的两个来源位置
# 可以为形状提供要显示的图像。
# 1 - 传递图像文件的本地文件系统文件名：
builder.write('Image from local file: ')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.writeln()
# 2 - 传递指向图像的 URL。
builder.write('Image from a URL: ')
builder.insert_image(file_name=IMAGE_URL)
builder.writeln()
doc.save(file_name=ARTIFACTS_DIR + 'Image.FromUrl.docx')
```

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个浮动图像，使其出现在重叠文本后面并对齐到页面中心。
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPageCenter.docx')
```

Shows how to insert WebP image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'WebP image.webp')
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertWebpImage.docx')
```

Shows how to insert an image from a stream into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
with system_helper.io.File.open_read(IMAGE_DIR + 'Logo.jpg') as stream:
    # 以下是从流中插入图像的三种方式。
    # 1 - 基于图像原始尺寸的默认大小的内联形状：
    builder.insert_image(stream=stream)
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    # 2 - 自定义尺寸的内联形状：
    builder.insert_image(stream=stream, width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    # 3 - 自定义尺寸的浮动形状：
    builder.insert_image(stream=stream, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertImageFromStream.docx')
```

Shows how to insert a shape with an image from a stream into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
with system_helper.io.File.open_read(IMAGE_DIR + 'Logo.jpg') as stream:
    builder.write('Image from stream: ')
    builder.insert_image(stream=stream)
doc.save(file_name=ARTIFACTS_DIR + 'Image.FromStream.docx')
```

Shows how to insert an image from a byte array into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_byte_array = test_util.TestUtil.image_to_byte_array(IMAGE_DIR + 'Logo.jpg')
# 以下是从字节数组中插入图像的三种方式。
# 1 - 基于图像原始尺寸的默认大小的内联形状：
builder.insert_image(image_bytes=image_byte_array)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 2 - 自定义尺寸的内联形状：
builder.insert_image(image_bytes=image_byte_array, width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 3 - 自定义尺寸的浮动形状：
builder.insert_image(image_bytes=image_byte_array, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertImageFromByteArray.docx')
```

Shows how to insert an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用文档生成器获取图像并将其插入为浮动形状有两种方法。
# 1 - 来自本地文件系统中的文件：
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=0, width=200, height=200, wrap_type=aw.drawing.WrapType.SQUARE)
# 2 - 来自 URL：
builder.insert_image(file_name=IMAGE_URL, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=250, width=200, height=200, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFloatingImage.docx')
```

Shows how to insert an image from the local file system into a document while preserving its dimensions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# InsertImage 方法创建一个浮动形状，其图像数据中包含传入的图像。
# 我们可以通过将尺寸传递给此方法来指定形状的尺寸。
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=0, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=0, width=-1, height=-1, wrap_type=aw.drawing.WrapType.SQUARE)
# 传递负值作为预期尺寸将自动定义
# 形状的尺寸将基于其图像的尺寸。
self.assertEqual(300, image_shape.width)
self.assertEqual(300, image_shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertImageOriginalSize.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

