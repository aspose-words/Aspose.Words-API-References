---
title: MarkdownSaveOptions.imagesFolder property
linktitle: imagesFolder property
articleTitle: imagesFolder property
second_title: Aspose.Words for NodeJs
description: "MarkdownSaveOptions.imagesFolder property. Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/markdownsaveoptions/imagesFolder/
---

## MarkdownSaveOptions.imagesFolder property

Specifies the physical folder where images are saved when exporting a document to
the [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format. Default is an empty string.



```js
get imagesFolder(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format,
Aspose.Words needs to save all images embedded in the document as standalone files.
[MarkdownSaveOptions.imagesFolder](./) allows you to specify where the images will be saved.


If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in
the same folder where the document file is saved. Use [MarkdownSaveOptions.imagesFolder](./) to override this behavior.


If you save a document into a stream, Aspose.Words does not have a folder
where to save the images, but still needs to save the images somewhere. In this case,
you need to specify an accessible folder in the [MarkdownSaveOptions.imagesFolder](./) property.


If the folder specified by [MarkdownSaveOptions.imagesFolder](./) doesn't exist, it will be created automatically.





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

