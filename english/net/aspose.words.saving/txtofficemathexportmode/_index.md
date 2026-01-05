---
title: TxtOfficeMathExportMode Enum
linktitle: TxtOfficeMathExportMode
articleTitle: TxtOfficeMathExportMode
second_title: Aspose.Words for .NET
description: TxtOfficeMathExportMode lets you choose how Word OfficeMath equations are exported to text for better accuracy and readability.
type: docs
weight: 6520
url: /net/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enumeration

Specifies how Aspose.Words exports OfficeMath to Text.

```csharp
public enum TxtOfficeMathExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | `0` | Export OfficeMath as plain text. |
| Latex | `3` | Export OfficeMath as LaTeX. |

## Examples

Shows how to export OfficeMath object as Latex in TXT.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

TxtSaveOptions saveOptions = new TxtSaveOptions();
saveOptions.OfficeMathExportMode = TxtOfficeMathExportMode.Latex;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
