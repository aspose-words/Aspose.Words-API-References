---
title: HtmlSaveOptions.imageResolution property
linktitle: imageResolution property
articleTitle: imageResolution property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.imageResolution property. Specifies the output resolution for images when exporting to HTML, MHTML or EPUB"
type: docs
weight: 340
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/imageResolution/
---

## HtmlSaveOptions.imageResolution property

Specifies the output resolution for images when exporting to HTML, MHTML or EPUB.
Default is ``96 dpi``.



```js
get imageResolution(): number
```

### Remarks

This property effects raster images when [HtmlSaveOptions.scaleImageToShapeSize](../scaleImageToShapeSize/) 
is ``true`` and effects metafiles exported as raster images. Some image properties such as cropping
or rotation require saving transformed images and in this case transformed images are created in the given
resolution.




### Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.words will create when saving a document to HTML.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let options = new aw.Saving.HtmlSaveOptions();
options.cssStyleSheetType = aw.Saving.CssStyleSheetType.External;
options.exportFontResources = true;
options.imageResolution = 72;
options.fontResourcesSubsettingSizeThreshold = 0;
options.fontsFolder = base.artifactsDir + "Fonts";
options.imagesFolder = base.artifactsDir + "Images";
options.resourceFolder = base.artifactsDir + "Resources";
options.fontsFolderAlias = "http://example.com/fonts";
options.imagesFolderAlias = "http://example.com/images";
options.resourceFolderAlias = "http://example.com/resources";
options.exportOriginalUrlForLinkedImages = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.scaleImageToShapeSize](../scaleImageToShapeSize/)

