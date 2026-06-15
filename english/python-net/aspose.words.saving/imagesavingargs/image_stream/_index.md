---
title: ImageSavingArgs.image_stream property
linktitle: image_stream property
articleTitle: image_stream property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.image_stream property. Allows to specify the stream where the image will be saved to."
type: docs
weight: 40
url: /python-net/aspose.words.saving/imagesavingargs/image_stream/
---

## ImageSavingArgs.image_stream property

Allows to specify the stream where the image will be saved to.


```python
@property
def image_stream(self) -> io.BytesIO:
    ...

@image_stream.setter
def image_stream(self, value: io.BytesIO):
    ...

```

### Remarks

This property allows you to save images to streams instead of files during HTML.

The default value is ``None``. When this property is ``None``, the image 
will be saved to a file specified in the [ImageSavingArgs.image_file_name](../image_file_name/) property.

Using [IImageSavingCallback](../../iimagesavingcallback/) you cannot substitute one image with 
another. It is intended only for control over location where to save images.




### Examples

Shows how to involve an image saving callback in an HTML conversion process (ImageShapePrinter).

```python
class ImageShapePrinter(aw.saving.IImageSavingCallback):

    def __init__(self):
        self.m_image_count = None

    def image_saving(self, args):
        args.keep_image_stream_open = False
        self.assertTrue(args.is_image_available)
        mImageCount += 1
        print(f'{Path(args.document.original_file_name).name} Image #{mImageCount}')
        layout_collector = aw.layout.LayoutCollector(args.document)
        print(f'\tOn page:\t{layout_collector.get_start_page_index(args.current_shape)}')
        print(f'\tDimensions:\t{args.current_shape.bounds}')
        print(f'\tAlignment:\t{args.current_shape.vertical_alignment}')
        print(f'\tWrap type:\t{args.current_shape.wrap_type}')
        print(f'Output filename:\t{args.image_file_name}\n')
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSavingArgs](../)
* property [ImageSavingArgs.image_file_name](../image_file_name/)
* property [ImageSavingArgs.keep_image_stream_open](../keep_image_stream_open/)

