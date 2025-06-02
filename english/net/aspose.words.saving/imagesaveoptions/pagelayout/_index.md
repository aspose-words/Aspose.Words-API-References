---
title: ImageSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words for .NET
description: ImageSaveOptions PageLayout property. Gets or sets the layout used when rendering multiple pages into a single output.
type: docs
weight: 100
url: /net/aspose.words.saving/imagesaveoptions/pagelayout/
---
## ImageSaveOptions.PageLayout property

Gets or sets the layout used when rendering multiple pages into a single output.

```csharp
public MultiPageLayout PageLayout { get; set; }
```

## Remarks

Use one of the factory methods of [`MultiPageLayout`](../../multipagelayout/) to configure this property.

For Tiff the default value is [`TiffFrames`](../../multipagelayout/tiffframes/). For other formats the default value is [`SinglePage`](../../multipagelayout/singlepage/).

This property has effect only when saving to the following formats: Jpeg, Gif, Png, Bmp, Tiff, WebP

### See Also

* class [MultiPageLayout](../../multipagelayout/)
* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
