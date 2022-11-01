---
title: is_image_available property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns ``True`` if the current image is available for export."
type: docs
weight: 50
url: /python-net/aspose.words.saving/imagesavingargs/is_image_available/
---

## ImageSavingArgs.is_image_available property

Returns ``True`` if the current image is available for export.


Some images in the document can be unavailable, for example, because the image
is linked and the link is inaccessible or does not point to a valid image. 
In this case Aspose.Words exports an icon with a red cross. This property returns 
``True`` if the original image is available; returns ``False`` if the original 
image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property 
is always ``True``.




### See Also

* module [aspose.words.saving](../../)
* class [ImageSavingArgs](../)
* property [ImageSavingArgs.current_shape](../current_shape/)

