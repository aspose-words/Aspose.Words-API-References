---
title: insert_image method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.DocumentBuilder.insert_image method"
type: docs
weight: 350
url: /python-net/aspose.words/documentbuilder/insert_image/
---

## insert_image(file_name) {#str}

Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.


```python
def insert_image(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

This overload will automatically download the image before inserting into the document
if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(stream) {#bytesio}

Inserts an image from a stream into the document. The image is inserted inline and at 100% scale.


```python
def insert_image(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(image_bytes) {#bytes}

Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.


```python
def insert_image(self, image_bytes: bytes):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(file_name, width, height) {#str_float_float}

Inserts an inline image from a file or URL into the document and scales it to the specified size.


```python
def insert_image(self, file_name: str, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| width | float |  |
| height | float |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(stream, width, height) {#bytesio_float_float}

Inserts an inline image from a stream into the document and scales it to the specified size.


```python
def insert_image(self, stream: BytesIO, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| width | float |  |
| height | float |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(image_bytes, width, height) {#bytes_float_float}

Inserts an inline image from a byte array into the document and scales it to the specified size.


```python
def insert_image(self, image_bytes: bytes, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_bytes | bytes |  |
| width | float |  |
| height | float |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(file_name, horz_pos, left, vert_pos, top, width, height, wrap_type) {#str_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an image from a file or URL at the specified position and size.


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

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(stream, horz_pos, left, vert_pos, top, width, height, wrap_type) {#bytesio_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an image from a stream at the specified position and size.


```python
def insert_image(self, stream: BytesIO, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | float |  |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | float |  |
| width | float |  |
| height | float |  |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_image(image_bytes, horz_pos, left, vert_pos, top, width, height, wrap_type) {#bytes_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an image from a byte array at the specified position and size.


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

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert an image from the local file system into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are three ways of inserting an image from a local system filename.
# 1 -  Inline shape with a default size based on the image's original dimensions:
builder.insert_image(IMAGE_DIR + "Logo.jpg")

builder.insert_break(aw.BreakType.PAGE_BREAK)

# 2 -  Inline shape with custom dimensions:
builder.insert_image(IMAGE_DIR + "Transparent background logo.png", aw.ConvertUtil.pixel_to_point(250),
    aw.ConvertUtil.pixel_to_point(144))

builder.insert_break(aw.BreakType.PAGE_BREAK)

# 3 -  Floating shape with custom dimensions:
builder.insert_image(IMAGE_DIR + "Windows MetaFile.wmf", aw.drawing.RelativeHorizontalPosition.MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.MARGIN, 100, 200, 100, aw.drawing.WrapType.SQUARE)

doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_image_from_filename.docx")
```

Shows how to determine which image will be inserted.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_image(IMAGE_DIR + "Scalable Vector Graphics.svg")

# Aspose.Words insert SVG image to the document as PNG with svgBlip extension
# that contains the original vector SVG image representation.
doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_svg_image.svg_with_svg_blip.docx")

# Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_svg_image.svg.doc")

doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)

# Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_svg_image.emf.docx")
```

Shows how to insert gif image to the document.

```python
builder = aw.DocumentBuilder()

# We can insert gif image using path or bytes array.
# It works only if DocumentBuilder optimized to Word version 2010 or higher.
# Note, that access to the image bytes causes conversion Gif to Png.
gif_image = builder.insert_image(IMAGE_DIR + "Graphics Interchange Format.gif")

with open(IMAGE_DIR + "Graphics Interchange Format.gif", "rb") as file:
    gif_image = builder.insert_image(file.read())

builder.document.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_gif.docx")
```

Shows how to insert a shape with an image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two locations where the document builder's "insert_image" method
# can source the image that the shape will display.
# 1 -  Pass a local file system filename of an image file:
builder.write("Image from local file: ")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.writeln()

# 2 -  Pass a URL which points to an image.
builder.write("Image from a URL: ")
builder.insert_image(IMAGE_URL)
builder.writeln()

doc.save(ARTIFACTS_DIR + "Image.from_url.docx")
```

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER

doc.save(ARTIFACTS_DIR + "Image.create_floating_page_center.docx")
```

Shows how to insert an image from a stream into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

with open(IMAGE_DIR + "Logo.jpg", "rb") as stream:

    # Below are three ways of inserting an image from a stream.
    # 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.insert_image(stream)

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # 2 -  Inline shape with custom dimensions:
    builder.insert_image(stream, aw.ConvertUtil.pixel_to_point(250), aw.ConvertUtil.pixel_to_point(144))

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # 3 -  Floating shape with custom dimensions:
    builder.insert_image(stream, aw.drawing.RelativeHorizontalPosition.MARGIN, 100, aw.drawing.RelativeVerticalPosition.MARGIN,
        100, 200, 100, aw.drawing.WrapType.SQUARE)

doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_image_from_stream.docx")
```

Shows how to insert a shape with an image from a stream into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

with open(IMAGE_DIR + "Logo.jpg", "rb") as stream:
    builder.write("Image from stream: ")
    builder.insert_image(stream)

doc.save(ARTIFACTS_DIR + "Image.from_stream.docx")
```

Shows how to insert an image from a byte array into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

image = drawing.Image.from_file(IMAGE_DIR + "Logo.jpg")

with io.BytesIO() as stream:

    image.save(stream, drawing.imaging.ImageFormat.png)
    image_byte_array = bytes(stream.getvalue())

    # Below are three ways of inserting an image from a byte array.
    # 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.insert_image(image_byte_array)

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # 2 -  Inline shape with custom dimensions:
    builder.insert_image(image_byte_array, aw.ConvertUtil.pixel_to_point(250), aw.ConvertUtil.pixel_to_point(144))

    builder.insert_break(aw.BreakType.PAGE_BREAK)

    # 3 -  Floating shape with custom dimensions:
    builder.insert_image(image_byte_array, aw.drawing.RelativeHorizontalPosition.MARGIN, 100, aw.drawing.RelativeVerticalPosition.MARGIN,
                         100, 200, 100, aw.drawing.WrapType.SQUARE)

doc.save(ARTIFACTS_DIR + "DocumentBuilderImages.insert_image_from_byte_array.docx")
```

Shows how to insert an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# There are two ways of using a document builder to source an image and then insert it as a floating shape.
# 1 -  From a file in the local file system:
builder.insert_image(IMAGE_DIR + "Transparent background logo.png", aw.drawing.RelativeHorizontalPosition.MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.MARGIN, 0, 200, 200, aw.drawing.WrapType.SQUARE)

# 2 -  From a URL:
builder.insert_image(IMAGE_URL, aw.drawing.RelativeHorizontalPosition.MARGIN, 100,
    aw.drawing.RelativeVerticalPosition.MARGIN, 250, 200, 200, aw.drawing.WrapType.SQUARE)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_floating_image.docx")
```

Shows how to insert an image from the local file system into a document while preserving its dimensions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# The "insert_image" method creates a floating shape with the passed image in its image data.
# We can specify the dimensions of the shape can be passing them to this method.
image_shape = builder.insert_image(IMAGE_DIR + "Logo.jpg", aw.drawing.RelativeHorizontalPosition.MARGIN, 0,
    aw.drawing.RelativeVerticalPosition.MARGIN, 0, -1, -1, aw.drawing.WrapType.SQUARE)

# Passing negative values as the intended dimensions will automatically define
# the shape's dimensions based on the dimensions of its image.
self.assertEqual(300.0, image_shape.width)
self.assertEqual(300.0, image_shape.height)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_image_original_size.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

