---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words JustificationMode-Aufzählung für präzise Zeichenabstandsanpassungen in Ihren Dokumenten. Verbessern Sie die Lesbarkeit mit anpassbaren Einstellungen!
type: docs
weight: 6630
url: /de/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Gibt die Zeichenabstandsanpassung für ein Dokument an. Der Standardwert ist`Expandieren` .

```csharp
public enum JustificationMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Expand | `0` | Zeichenabstand nicht komprimieren. |
| Compress | `1` | Zeichenabstand komprimieren. |
| CompressKana | `2` | Komprimieren Sie unter Verwendung der Regeln der Kana-Silbenschriften Hiragana und Katakana. |

## Beispiele

Zeigt, wie die Steuerung des Zeichenabstands verwaltet wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
