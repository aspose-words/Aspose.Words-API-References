---
title: HtmlSaveOptions.resourceFolderAlias property
linktitle: resourceFolderAlias property
articleTitle: resourceFolderAlias property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.resourceFolderAlias property. Specifies the name of the folder used to construct URIs of all resources written into an HTML document"
type: docs
weight: 440
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/resourceFolderAlias/
---

## HtmlSaveOptions.resourceFolderAlias property

Specifies the name of the folder used to construct URIs of all resources written into an HTML document.
Default is an empty string.


```js
get resourceFolderAlias(): string
```

### Remarks

[HtmlSaveOptions.resourceFolderAlias](./) is the simplest way to specify how URIs for all resource files should be
constructed. Same information can be specified for images and fonts separately via [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/)
and [HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/) properties, respectively. However, there is no individual property for CSS.


[HtmlSaveOptions.resourceFolderAlias](./) has lower priority than [HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/)
and [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/). For example, if both [HtmlSaveOptions.resourceFolderAlias](./)
and [HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/) are specified, fonts' URIs will be constructed using
[HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/), while URIs of images and CSS will be constructed using
[HtmlSaveOptions.resourceFolderAlias](./).

If [HtmlSaveOptions.resourceFolderAlias](./) is empty, the [HtmlSaveOptions.resourceFolder](../resourceFolder/) property value will be used
to construct resource URIs.

If [HtmlSaveOptions.resourceFolderAlias](./) is set to '.' (dot), resource URIs will contain file names only, without
any path.




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
* property [HtmlSaveOptions.fontsFolderAlias](../fontsFolderAlias/)
* property [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/)

