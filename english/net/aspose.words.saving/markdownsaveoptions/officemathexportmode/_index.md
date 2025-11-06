---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words for .NET
description: Discover the MarkdownSaveOptions OfficeMathExportMode property to customize OfficeMath output. Optimize your files with flexible export settings!
type: docs
weight: 120
url: /net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Specifies how OfficeMath will be written to the output file. Default value is Text.

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Examples

Shows how OfficeMath will be written to the document.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

Shows how to export OfficeMath object as Latex.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Latex;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```

Shows how to export OfficeMath object as MarkItDown.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.MarkItDown;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

### See Also

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
