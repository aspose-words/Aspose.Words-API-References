---
title: current_shape property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved."
type: docs
weight: 10
url: /python-net/aspose.words.saving/imagesavingargs/current_shape/
---

## ImageSavingArgs.current_shape property

Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape 
that is about to be saved.


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




### See Also

* module [aspose.words.saving](../../)
* class [ImageSavingArgs](../)

