---
title: ImageSavingArgs.keep_image_stream_open property
linktitle: keep_image_stream_open property
articleTitle: keep_image_stream_open property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.keep_image_stream_open property. Specifies whether Aspose.Words should keep the stream open or close it after saving an image."
type: docs
weight: 60
url: /python-net/aspose.words.saving/imagesavingargs/keep_image_stream_open/
---

## ImageSavingArgs.keep_image_stream_open property

Specifies whether Aspose.Words should keep the stream open or close it after saving an image.


```python
@property
def keep_image_stream_open(self) -> bool:
    ...

@keep_image_stream_open.setter
def keep_image_stream_open(self, value: bool):
    ...

```

### Remarks

Default is ``False`` and Aspose.Words will close the stream you provided
in the [ImageSavingArgs.image_stream](../image_stream/) property after writing an image into it.
Specify ``True`` to keep the stream open.




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
* property [ImageSavingArgs.image_stream](../image_stream/)

