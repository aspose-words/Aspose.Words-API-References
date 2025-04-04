---
title: HtmlSaveOptions.imagesFolderAlias property
linktitle: imagesFolderAlias property
articleTitle: imagesFolderAlias property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.imagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an HTML document"
type: docs
weight: 370
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/imagesFolderAlias/
---

## HtmlSaveOptions.imagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an HTML document.
Default is an empty string.


```js
get imagesFolderAlias(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [HtmlSaveOptions.imagesFolder](../imagesFolder/) 
allows you to specify where the images will be saved and [HtmlSaveOptions.imagesFolderAlias](./) 
allows to specify how the image URIs will be constructed.

If [HtmlSaveOptions.imagesFolderAlias](./) is not an empty string, then the image URI written
to HTML will be *ImagesFolderAlias + \<image file name\>*.

If [HtmlSaveOptions.imagesFolderAlias](./) is an empty string, then the image URI written 
to HTML will be *ImagesFolder + \<image file name\>*.

If [HtmlSaveOptions.imagesFolderAlias](./) is set to '.' (dot), then the image file name 
will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs
is to use [HtmlSaveOptions.resourceFolderAlias](../resourceFolderAlias/).




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
* property [HtmlSaveOptions.resourceFolderAlias](../resourceFolderAlias/)
* property [HtmlSaveOptions.imagesFolder](../imagesFolder/)
* property [HtmlSaveOptions.imageSavingCallback](../imageSavingCallback/)

