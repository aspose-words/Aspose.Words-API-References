---
title: MarkdownSaveOptions.imagesFolder property
linktitle: imagesFolder property
articleTitle: imagesFolder property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.imagesFolder property. Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format"
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/imagesFolder/
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





### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

