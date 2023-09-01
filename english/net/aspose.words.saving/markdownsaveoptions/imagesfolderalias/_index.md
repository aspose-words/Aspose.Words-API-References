---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: MarkdownSaveOptions ImagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in Markdown format, Aspose.Words needs to save all images embedded in the document as standalone files. [`ImagesFolder`](../imagesfolder/) allows you to specify where the images will be saved and `ImagesFolderAlias` allows to specify how the image URIs will be constructed.

If `ImagesFolderAlias` is not an empty string, then the image URI written to Markdown will be ImagesFolderAlias + &lt;image file name&gt;.

If `ImagesFolderAlias` is an empty string, then the image URI written to Markdown will be ImagesFolder + &lt;image file name&gt;.

If `ImagesFolderAlias` is set to '.' (dot), then the image file name will be written to Markdown without path regardless of other options.

### See Also

* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
