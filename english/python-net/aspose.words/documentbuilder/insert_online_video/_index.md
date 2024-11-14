---
title: DocumentBuilder.insert_online_video method
linktitle: insert_online_video method
articleTitle: insert_online_video method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_online_video method"
type: docs
weight: 440
url: /python-net/aspose.words/documentbuilder/insert_online_video/
---

## insert_online_video(video_url, width, height) {#str_float_float}

Inserts an online video object into the document and scales it to the specified size.


```python
def insert_online_video(self, video_url: str, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| video_url | str | The URL to the video. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.

Insertion of online video from the following resources is supported:


* https://www.youtube.com/
  
* https://vimeo.com/
  
If your online video is not displaying correctly, use [DocumentBuilder.insert_online_video()](./#str_str_bytes_float_float), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.




### Returns

The image node that was just inserted.


## insert_online_video(video_url, horz_pos, left, vert_pos, top, width, height, wrap_type) {#str_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an online video object into the document and scales it to the specified size.


```python
def insert_online_video(self, video_url: str, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| video_url | str | The URL to the video. |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | float | Distance in points from the origin to the left side of the image. |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | float | Distance in points from the origin to the top side of the image. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.

Insertion of online video from the following resources is supported:


* https://www.youtube.com/
  
* https://vimeo.com/
  
If your online video is not displaying correctly, use [DocumentBuilder.insert_online_video()](./#str_str_bytes_float_float), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.




### Returns

The image node that was just inserted.


## insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, width, height) {#str_str_bytes_float_float}

Inserts an online video object into the document and scales it to the specified size.


```python
def insert_online_video(self, video_url: str, video_embed_code: str, thumbnail_image_bytes: bytes, width: float, height: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| video_url | str | The URL to the video. |
| video_embed_code | str | The embed code for the video. |
| thumbnail_image_bytes | bytes | The thumbnail image bytes. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, horz_pos, left, vert_pos, top, width, height, wrap_type) {#str_str_bytes_relativehorizontalposition_float_relativeverticalposition_float_float_float_wraptype}

Inserts an online video object into the document and scales it to the specified size.


```python
def insert_online_video(self, video_url: str, video_embed_code: str, thumbnail_image_bytes: bytes, horz_pos: aspose.words.drawing.RelativeHorizontalPosition, left: float, vert_pos: aspose.words.drawing.RelativeVerticalPosition, top: float, width: float, height: float, wrap_type: aspose.words.drawing.WrapType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| video_url | str | The URL to the video. |
| video_embed_code | str | The embed code for the video. |
| thumbnail_image_bytes | bytes | The thumbnail image bytes. |
| horz_pos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | float | Distance in points from the origin to the left side of the image. |
| vert_pos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | float | Distance in points from the origin to the top side of the image. |
| width | float | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | float | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrap_type | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert an online video into a document using a URL.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_online_video(video_url='https://youtu.be/g1N9ke8Prmk', width=360, height=270)
# We can watch the video from Microsoft Word by clicking on the shape.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertVideoWithUrl.docx')
```

Shows how to insert an online video into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
video_url = 'https://vimeo.com/52477838'
# Insert a shape that plays a video from the web when clicked in Microsoft Word.
# This rectangular shape will contain an image based on the first frame of the linked video
# and a "play button" visual prompt. The video has an aspect ratio of 16:9.
# We will set the shape's size to that ratio, so the image does not appear stretched.
builder.insert_online_video(video_url=video_url, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=0, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=0, width=320, height=180, wrap_type=aw.drawing.WrapType.SQUARE)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertOnlineVideo.docx')
```

Shows how to insert an online video into a document with a custom thumbnail.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
video_url = 'https://vimeo.com/52477838'
video_embed_code = '<iframe src="https://player.vimeo.com/video/52477838" width="640" height="360" frameborder="0" ' + 'title="Aspose" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>'
with open(IMAGE_DIR + 'Logo.jpg', 'rb') as file:
    thumbnail_image_bytes = file.read()
    image = aspose.pydrawing.Image.from_stream(io.BytesIO(thumbnail_image_bytes))
    # Below are two ways of creating a shape with a custom thumbnail, which links to an online video
    # that will play when we click on the shape in Microsoft Word.
    # 1 -  Insert an inline shape at the builder's node insertion cursor:
    builder.insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, image.width, image.height)
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    # 2 -  Insert a floating shape:
    left = builder.page_setup.right_margin - image.width
    top = builder.page_setup.bottom_margin - image.height
    builder.insert_online_video(video_url, video_embed_code, thumbnail_image_bytes, aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left, aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top, image.width, image.height, aw.drawing.WrapType.SQUARE)
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.insert_online_video_custom_thumbnail.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

