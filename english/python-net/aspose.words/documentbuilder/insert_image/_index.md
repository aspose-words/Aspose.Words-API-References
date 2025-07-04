﻿---
title: DocumentBuilder.insert_image method
linktitle: insert_image method
articleTitle: insert_image method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_image method"
type: docs
weight: 400
url: /python-net/aspose.words/documentbuilder/insert_image/
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
# Below are three ways of inserting an image from a local system filename.
# 1 -  Inline shape with a default size based on the image's original dimensions:
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 2 -  Inline shape with custom dimensions:
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png', width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 3 -  Floating shape with custom dimensions:
builder.insert_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertImageFromFilename.docx')
```

Shows how to determine which image will be inserted.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Scalable Vector Graphics.svg')
# Aspose.Words insert SVG image to the document as PNG with svgBlip extension
# that contains the original vector SVG image representation.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx')
# Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.Svg.doc')
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
# Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertSvgImage.Emf.docx')
```

Shows how to insert gif image to the document.

```python
builder = aw.DocumentBuilder()
# We can insert gif image using path or bytes array.
# It works only if DocumentBuilder optimized to Word version 2010 or higher.
# Note, that access to the image bytes causes conversion Gif to Png.
gif_image = builder.insert_image(file_name=IMAGE_DIR + 'Graphics Interchange Format.gif')
gif_image = builder.insert_image(image_bytes=system_helper.io.File.read_all_bytes(IMAGE_DIR + 'Graphics Interchange Format.gif'))
builder.document.save(file_name=ARTIFACTS_DIR + 'InsertGif.docx')
```

Shows how to insert a shape with an image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Below are two locations where the document builder's "InsertShape" method
# can source the image that the shape will display.
# 1 -  Pass a local file system filename of an image file:
builder.write('Image from local file: ')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.writeln()
# 2 -  Pass a URL which points to an image.
builder.write('Image from a URL: ')
builder.insert_image(file_name=IMAGE_URL)
builder.writeln()
doc.save(file_name=ARTIFACTS_DIR + 'Image.FromUrl.docx')
```

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
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
    # Below are three ways of inserting an image from a stream.
    # 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.insert_image(stream=stream)
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    # 2 -  Inline shape with custom dimensions:
    builder.insert_image(stream=stream, width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    # 3 -  Floating shape with custom dimensions:
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
# Below are three ways of inserting an image from a byte array.
# 1 -  Inline shape with a default size based on the image's original dimensions:
builder.insert_image(image_bytes=image_byte_array)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 2 -  Inline shape with custom dimensions:
builder.insert_image(image_bytes=image_byte_array, width=aw.ConvertUtil.pixel_to_point(pixels=250), height=aw.ConvertUtil.pixel_to_point(pixels=144))
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 3 -  Floating shape with custom dimensions:
builder.insert_image(image_bytes=image_byte_array, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=100, width=200, height=100, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilderImages.InsertImageFromByteArray.docx')
```

Shows how to insert an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# There are two ways of using a document builder to source an image and then insert it as a floating shape.
# 1 -  From a file in the local file system:
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=0, width=200, height=200, wrap_type=aw.drawing.WrapType.SQUARE)
# 2 -  From a URL:
builder.insert_image(file_name=IMAGE_URL, horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=250, width=200, height=200, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFloatingImage.docx')
```

Shows how to insert an image from the local file system into a document while preserving its dimensions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# The InsertImage method creates a floating shape with the passed image in its image data.
# We can specify the dimensions of the shape can be passing them to this method.
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg', horz_pos=aw.drawing.RelativeHorizontalPosition.MARGIN, left=0, vert_pos=aw.drawing.RelativeVerticalPosition.MARGIN, top=0, width=-1, height=-1, wrap_type=aw.drawing.WrapType.SQUARE)
# Passing negative values as the intended dimensions will automatically define
# the shape's dimensions based on the dimensions of its image.
self.assertEqual(300, image_shape.width)
self.assertEqual(300, image_shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertImageOriginalSize.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

