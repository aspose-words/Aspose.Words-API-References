---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words for .NET
description: MarkdownSaveOptions ExportImagesAsBase64 property. Specifies whether images are saved in Base64 format to the output file. Default value is false in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Specifies whether images are saved in Base64 format to the output file. Default value is `false`.

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Remarks

When this property is set to `true` images data are exported directly into the **img** elements and separate files are not created.

## Examples

Shows how to save a .md document with images embedded inside it.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### See Also

* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
