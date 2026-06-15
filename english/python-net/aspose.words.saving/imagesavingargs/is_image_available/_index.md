---
title: ImageSavingArgs.is_image_available property
linktitle: is_image_available property
articleTitle: is_image_available property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.is_image_available property. Returns ``True`` if the current image is available for export."
type: docs
weight: 50
url: /python-net/aspose.words.saving/imagesavingargs/is_image_available/
---

## ImageSavingArgs.is_image_available property

Returns ``True`` if the current image is available for export.



```python
@property
def is_image_available(self) -> bool:
    ...

```

### Remarks

Some images in the document can be unavailable, for example, because the image
is linked and the link is inaccessible or does not point to a valid image. 
In this case Aspose.Words exports an icon with a red cross. This property returns 
``True`` if the original image is available; returns ``False`` if the original 
image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property 
is always ``True``.




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
* property [ImageSavingArgs.current_shape](../current_shape/)

