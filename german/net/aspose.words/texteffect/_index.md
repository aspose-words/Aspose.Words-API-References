---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.TextEffect für dynamische Textanimationen. Verbessern Sie Ihre Dokumente mit ansprechenden Effekten für ein fesselndes Benutzererlebnis.
type: docs
weight: 7270
url: /de/net/aspose.words/texteffect/
---
## TextEffect enumeration

Animationseffekt für Textläufe.

```csharp
public enum TextEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Beispiele

Zeigt, wie man einem Lauf einen visuellen Effekt zuweist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Ältere Versionen von Microsoft Word unterstützen nur Schriftanimationseffekte.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
