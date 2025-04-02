---
title: HtmlSaveOptions.resourceFolder property
linktitle: resourceFolder property
articleTitle: resourceFolder property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.resourceFolder property. Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML"
type: docs
weight: 430
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/resourceFolder/
---

## HtmlSaveOptions.resourceFolder property

Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document
is exported to HTML. Default is an empty string.


```js
get resourceFolder(): string
```

### Remarks

[HtmlSaveOptions.resourceFolder](./) is the simplest way to specify a folder where all resources should be written.
Another way is to use individual properties [HtmlSaveOptions.fontsFolder](../fontsFolder/), [HtmlSaveOptions.imagesFolder](../imagesFolder/),
and [HtmlSaveOptions.cssStyleSheetFileName](../cssStyleSheetFileName/).

[HtmlSaveOptions.resourceFolder](./) has a lower priority than folders specified via [HtmlSaveOptions.fontsFolder](../fontsFolder/),
[HtmlSaveOptions.imagesFolder](../imagesFolder/), and [HtmlSaveOptions.cssStyleSheetFileName](../cssStyleSheetFileName/). For example, if both
[HtmlSaveOptions.resourceFolder](./) and [HtmlSaveOptions.fontsFolder](../fontsFolder/) are specified, fonts will be saved
to [HtmlSaveOptions.fontsFolder](../fontsFolder/), while images and CSS will be saved to [HtmlSaveOptions.resourceFolder](./).

If the folder specified by [HtmlSaveOptions.resourceFolder](./) doesn't exist, it will be created automatically.





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
* property [HtmlSaveOptions.fontsFolder](../fontsFolder/)
* property [HtmlSaveOptions.imagesFolder](../imagesFolder/)
* property [HtmlSaveOptions.cssStyleSheetFileName](../cssStyleSheetFileName/)

