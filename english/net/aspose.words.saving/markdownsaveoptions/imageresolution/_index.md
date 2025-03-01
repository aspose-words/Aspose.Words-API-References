---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words for .NET
description: Optimize your Markdown exports with the ImageResolution property, setting custom output resolutions for sharper images. Default, 96 dpi.
type: docs
weight: 50
url: /net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Specifies the output resolution for images when exporting to Markdown. Default is `96 dpi`.

```csharp
public int ImageResolution { get; set; }
```

## Examples

Shows how to set the output resolution for images.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### See Also

* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
