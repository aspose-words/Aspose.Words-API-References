---
title: ImageSaveOptions.pageLayout property
linktitle: pageLayout property
articleTitle: pageLayout property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.pageLayout property. Gets or sets the layout used when rendering multiple pages into a single output."
type: docs
weight: 90
url: /nodejs-net/aspose.words.saving/imagesaveoptions/pageLayout/
---

## ImageSaveOptions.pageLayout property

Gets or sets the layout used when rendering multiple pages into a single output.


```js
get pageLayout(): Aspose.Words.Saving.MultiPageLayout
```

### Remarks

Use one of the factory methods of [MultiPageLayout](../../multipagelayout/) to configure this property.


For [SaveFormat.Tiff](../../../aspose.words/saveformat/#Tiff) the default value is [MultiPageLayout.tiffFrames()](../../multipagelayout/tiffFrames/#default).
For other formats the default value is [MultiPageLayout.singlePage()](../../multipagelayout/singlePage/#default).


This property has effect only when saving to the following formats:
[SaveFormat.Jpeg](../../../aspose.words/saveformat/#Jpeg), [SaveFormat.Gif](../../../aspose.words/saveformat/#Gif), [SaveFormat.Png](../../../aspose.words/saveformat/#Png),
[SaveFormat.Bmp](../../../aspose.words/saveformat/#Bmp), [SaveFormat.Tiff](../../../aspose.words/saveformat/#Tiff), [SaveFormat.WebP](../../../aspose.words/saveformat/#WebP)





### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

