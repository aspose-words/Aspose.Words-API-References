---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LowCode.MergeFormatMode enum för att optimera dokumentsammanfogning. Förbättra formateringskontrollen när du kombinerar flera filer utan problem.
type: docs
weight: 4290
url: /sv/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Anger hur formatering slås samman när flera dokument kombineras.

```csharp
public enum MergeFormatMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| MergeFormatting | `0` | Kombinera formateringen av de sammanslagna dokumenten. |
| KeepSourceFormatting | `1` | Innebär att källdokumentet behåller sin ursprungliga formatering, såsom teckensnitt, storlekar, färger, indrag och andra formateringselement som tillämpats på innehållet. |
| KeepSourceLayout | `2` | Bevara layouten från originaldokumenten i det slutliga dokumentet. |

## Exempel

Visar hur man sammanfogar dokument till ett enda utdatadokument.

```csharp
//Det finns flera sätt att sammanfoga dokument:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Se även

* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
