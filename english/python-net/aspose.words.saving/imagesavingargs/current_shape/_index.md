---
title: ImageSavingArgs.current_shape property
linktitle: current_shape property
articleTitle: current_shape property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.current_shape property. Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved."
type: docs
weight: 10
url: /python-net/aspose.words.saving/imagesavingargs/current_shape/
---

## ImageSavingArgs.current_shape property

Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape 
that is about to be saved.



```python
@property
def current_shape(self) -> aspose.words.drawing.ShapeBase:
    ...

```

### Remarks

[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. 
That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing 
[ShapeBase.shape_type](../../../aspose.words.drawing/shapebase/shape_type/) with [ShapeType.GROUP](../../../aspose.words.drawing/shapetype/#GROUP) or by casting it to one of derived classes: 
[Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name 
for each image found in the document. You can use the [ImageSavingArgs.current_shape](./) property to generate 
a "better" file name by examining shape properties such as [ImageData.title](../../../aspose.words.drawing/imagedata/title/) 
(Shape only), [ImageData.source_full_name](../../../aspose.words.drawing/imagedata/source_full_name/) (Shape only) 
and [ShapeBase.name](../../../aspose.words.drawing/shapebase/name/). Of course you can build file names using any other properties or criteria 
but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability 
use the [ImageSavingArgs.is_image_available](../is_image_available/) property.




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

