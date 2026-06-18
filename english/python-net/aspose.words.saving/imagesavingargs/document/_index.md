---
title: ImageSavingArgs.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.document property. Gets the document object that is currently being saved."
type: docs
weight: 20
url: /python-net/aspose.words.saving/imagesavingargs/document/
---

## ImageSavingArgs.document property

Gets the document object that is currently being saved.


```python
@property
def document(self) -> aspose.words.Document:
    ...

```

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

