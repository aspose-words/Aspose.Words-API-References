---
title: HtmlSaveOptions.exportOriginalUrlForLinkedImages property
linktitle: exportOriginalUrlForLinkedImages property
articleTitle: exportOriginalUrlForLinkedImages property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.exportOriginalUrlForLinkedImages property. Specifies whether original URL should be used as the URL of the linked images"
type: docs
weight: 200
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportOriginalUrlForLinkedImages/
---

## HtmlSaveOptions.exportOriginalUrlForLinkedImages property

Specifies whether original URL should be used as the URL of the linked images.
Default value is ``false``.



```js
get exportOriginalUrlForLinkedImages(): boolean
```

### Remarks

If value is set to ``true``
[ImageData.sourceFullName](../../../aspose.words.drawing/imagedata/sourceFullName/) value is used
as the URL of linked images and linked images are not loaded into document's folder
or [HtmlSaveOptions.imagesFolder](../imagesFolder/).

If value is set to ``false`` linked images are loaded into document's folder
or [HtmlSaveOptions.imagesFolder](../imagesFolder/) and URL of each linked image is constructed depending
on document's folder, [HtmlSaveOptions.imagesFolder](../imagesFolder/) 
and [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/) properties.




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

