---
title: TxtSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words for .NET
description: Control how OfficeMath is written in TXT output with OfficeMathExportMode for consistent formatting and clear mathematical content.
type: docs
weight: 50
url: /net/aspose.words.saving/txtsaveoptions/officemathexportmode/
---
## TxtSaveOptions.OfficeMathExportMode property

Specifies how OfficeMath will be written to the output file. Default value is Text.

```csharp
public TxtOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Examples

Shows how to export OfficeMath object as Latex in TXT.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

TxtSaveOptions saveOptions = new TxtSaveOptions();
saveOptions.OfficeMathExportMode = TxtOfficeMathExportMode.Latex;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

### See Also

* enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* class [TxtSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
