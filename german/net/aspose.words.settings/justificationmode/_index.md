---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words für .NET
description: Aspose.Words.Settings.JustificationMode opsomming. Gibt die Anpassung des Zeichenabstands für ein Dokument an. Der Standardwert istExpandieren  in C#.
type: docs
weight: 5800
url: /de/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Gibt die Anpassung des Zeichenabstands für ein Dokument an. Der Standardwert ist`Expandieren` .

```csharp
public enum JustificationMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

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
