---
title: MarkdownSaveOptions.imagesFolderAlias property
linktitle: imagesFolderAlias property
articleTitle: imagesFolderAlias property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.imagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into a document"
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/imagesFolderAlias/
---

## MarkdownSaveOptions.imagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into a document.
Default is an empty string.


```js
get imagesFolderAlias(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format,
Aspose.Words needs to save all images embedded in the document as standalone files.
[MarkdownSaveOptions.imagesFolder](../imagesFolder/) allows you to specify where the images will be saved and
[MarkdownSaveOptions.imagesFolderAlias](./) allows to specify how the image URIs will be constructed.

If [MarkdownSaveOptions.imagesFolderAlias](./) is not an empty string, then the image URI written
to Markdown will be *ImagesFolderAlias + \<image file name\>*.

If [MarkdownSaveOptions.imagesFolderAlias](./) is an empty string, then the image URI written
to Markdown will be *ImagesFolder + \<image file name\>*.

If [MarkdownSaveOptions.imagesFolderAlias](./) is set to '.' (dot), then the image file name
will be written to Markdown without path regardless of other options.




### Examples

Shows how to specifies the name of the folder used to construct image URIs.

```js
let builder = new aw.DocumentBuilder();

builder.writeln("Some image below:");            
builder.insertImage(base.imageDir + "Logo.jpg");

string imagesFolder = Path.Combine(base.artifactsDir, "ImagesDir");
let saveOptions = new aw.Saving.MarkdownSaveOptions();
// Use the "ImagesFolder" property to assign a folder in the local file system into which
// Aspose.words will save all the document's linked images.
saveOptions.imagesFolder = imagesFolder;
// Use the "ImagesFolderAlias" property to use this folder
// when constructing image URIs instead of the images folder's name.
saveOptions.imagesFolderAlias = "http://example.com/images";

builder.document.save(base.artifactsDir + "MarkdownSaveOptions.imagesFolder.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)
* property [MarkdownSaveOptions.imagesFolder](../imagesFolder/)
* property [MarkdownSaveOptions.imageSavingCallback](../imageSavingCallback/)

