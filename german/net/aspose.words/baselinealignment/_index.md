---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words für .NET
description: Aspose.Words.BaselineAlignment opsomming. Gibt die vertikale Position der Schriftarten in einer Zeile an in C#.
type: docs
weight: 20
url: /de/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Gibt die vertikale Position der Schriftarten in einer Zeile an.

```csharp
public enum BaselineAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Top | `0` | Wird am oberen Rand jeder Schriftart ausgerichtet. |
| Center | `1` | Richtet die Mittelpunkte jeder Schriftart aus. |
| Baseline | `2` | Wird an der Grundlinie des Absatzes ausgerichtet. |
| Bottom | `3` | Wird am unteren Rand jeder Schriftart ausgerichtet. |
| Auto | `4` | Die Grundlinie wird automatisch angepasst. |

## Beispiele

Zeigt, wie die vertikale Position von Schriftarten in einer Zeile festgelegt wird.

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
