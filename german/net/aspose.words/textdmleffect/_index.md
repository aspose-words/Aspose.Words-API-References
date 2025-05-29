---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.TextDmlEffect zur Verbesserung von Textläufen mit dynamischen DML-Effekten. Verbessern Sie mühelos die Präsentation Ihrer Dokumente!
type: docs
weight: 7260
url: /de/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Dml-Texteffekt für Textläufe.

```csharp
public enum TextDmlEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Glow | `0` | Leuchteffekt, bei dem außerhalb der Kanten des Objekts ein farbig verwischter Umriss hinzugefügt wird. |
| Fill | `1` | Füllüberlagerungseffekt. |
| Shadow | `2` | Schatteneffekt. |
| Outline | `3` | Umrisseffekt. |
| Effect3D | `4` | 3D-Effekt. |
| Reflection | `5` | Reflexionseffekt. |

## Beispiele

Zeigt, wie überprüft wird, ob ein Lauf einen DrawingML-Texteffekt anzeigt.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
