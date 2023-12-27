---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words for .NET
description: MarkdownSaveOptions ExportUnderlineFormatting property. Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters . The default value is false in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is `false`.

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Examples

Shows how to export underline formatting as ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### See Also

* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
