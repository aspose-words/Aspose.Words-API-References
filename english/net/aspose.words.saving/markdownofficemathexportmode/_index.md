---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words for .NET
description: Discover how Aspose.Words.Saving.MarkdownOfficeMathExportMode enhances OfficeMath export to Markdown, ensuring accurate and efficient document conversion.
type: docs
weight: 6080
url: /net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Specifies how Aspose.Words exports OfficeMath to Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | `0` | Export OfficeMath as plain text. |
| Image | `1` | Export OfficeMath as image. |
| MathML | `2` | Export OfficeMath as MathML. |
| Latex | `3` | Export OfficeMath as LaTeX. |

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

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
