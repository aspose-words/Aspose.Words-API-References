---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.BaselineAlignment für präzise Schriftpositionierung. Verbessern Sie die Formatierung Ihres Dokuments mit optimalen vertikalen Ausrichtungsoptionen.
type: docs
weight: 130
url: /de/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Gibt die vertikale Position der Schriftart in einer Zeile an.

```csharp
public enum BaselineAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Top | `0` | Richtet die Schriftart oben an jeder Schriftart aus. |
| Center | `1` | Richtet die Mittelpunkte jeder Schriftart aus. |
| Baseline | `2` | Richtet sich an der Grundlinie des Absatzes aus. |
| Bottom | `3` | Richtet sich am unteren Rand jeder Schriftart aus. |
| Auto | `4` | Die Basislinie wird automatisch angepasst. |

## Beispiele

Zeigt, wie die vertikale Position von Schriftarten auf einer Zeile festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
