---
title: HtmlSaveOptions.fontsFolder property
linktitle: fontsFolder property
articleTitle: fontsFolder property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.fontsFolder property. Specifies the physical folder where fonts are saved when exporting a document to HTML"
type: docs
weight: 310
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/fontsFolder/
---

## HtmlSaveOptions.fontsFolder property

Specifies the physical folder where fonts are saved when exporting a document to HTML.
Default is an empty string.


```js
get fontsFolder(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in HTML format and [HtmlSaveOptions.exportFontResources](../exportFontResources/) 
is set to ``True``, Aspose.Words needs to save fonts used in the document as standalone files. 
[HtmlSaveOptions.fontsFolder](./) allows you to specify where the fonts will be saved and 
[HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
fonts in the same folder where the document file is saved. Use [HtmlSaveOptions.fontsFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, 
but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder 
in the [HtmlSaveOptions.fontsFolder](./) property or provide custom streams via 
the [HtmlSaveOptions.fontSavingCallback](../fontSavingCallback/) event handler.

If the folder specified by [HtmlSaveOptions.fontsFolder](./) doesn't exist, it will be created automatically.

[HtmlSaveOptions.resourceFolder](../resourceFolder/) is another way to specify a folder where fonts should be saved.




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
* property [HtmlSaveOptions.resourceFolder](../resourceFolder/)
* property [HtmlSaveOptions.exportFontResources](../exportFontResources/)
* property [HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/)
* property [HtmlSaveOptions.fontSavingCallback](../fontSavingCallback/)

