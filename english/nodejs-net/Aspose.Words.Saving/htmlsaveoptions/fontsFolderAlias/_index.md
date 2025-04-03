---
title: HtmlSaveOptions.fontsFolderAlias property
linktitle: fontsFolderAlias property
articleTitle: fontsFolderAlias property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.fontsFolderAlias property. Specifies the name of the folder used to construct font URIs written into an HTML document"
type: docs
weight: 320
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/fontsFolderAlias/
---

## HtmlSaveOptions.fontsFolderAlias property

Specifies the name of the folder used to construct font URIs written into an HTML document.
Default is an empty string.


```js
get fontsFolderAlias(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in HTML format and [HtmlSaveOptions.exportFontResources](../exportFontResources/) 
is set to ``true``, Aspose.Words needs to save fonts used in the document as standalone files. 
[HtmlSaveOptions.fontsFolder](../fontsFolder/) allows you to specify where the fonts will be saved and 
[HtmlSaveOptions.fontsFolderAlias](./) allows to specify how the font URIs will be constructed.

If [HtmlSaveOptions.fontsFolderAlias](./) is not an empty string, then the font URI written
to HTML will be *FontsFolderAlias + \<font file name\>*.

If [HtmlSaveOptions.fontsFolderAlias](./) is an empty string, then the font URI written 
to HTML will be *FontsFolder + \<font file name\>*.

If [HtmlSaveOptions.fontsFolderAlias](./) is set to '.' (dot), then the font file name 
will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs
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
* property [HtmlSaveOptions.exportFontResources](../exportFontResources/)
* property [HtmlSaveOptions.fontsFolder](../fontsFolder/)
* property [HtmlSaveOptions.fontSavingCallback](../fontSavingCallback/)

