---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.LowCode.MergeFormatMode, um das Zusammenführen von Dokumenten zu optimieren. Verbessern Sie die Formatierungskontrolle beim mühelosen Zusammenführen mehrerer Dateien.
type: docs
weight: 4290
url: /de/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Gibt an, wie die Formatierung beim Kombinieren mehrerer Dokumente zusammengeführt wird.

```csharp
public enum MergeFormatMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| MergeFormatting | `0` | Kombinieren Sie die Formatierung der zusammengeführten Dokumente. |
| KeepSourceFormatting | `1` | Bedeutet, dass das Quelldokument seine ursprüngliche Formatierung beibehält, wie Schriftarten, -größen, -farben, Einzüge und alle anderen auf den Inhalt angewendeten Formatierungselemente. |
| KeepSourceLayout | `2` | Behalten Sie das Layout der Originaldokumente im endgültigen Dokument bei. |

## Beispiele

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```csharp
//Es gibt mehrere Möglichkeiten, Dokumente zusammenzuführen:
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

### Siehe auch

* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
