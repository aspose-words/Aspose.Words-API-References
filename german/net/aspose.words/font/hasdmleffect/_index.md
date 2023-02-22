---
title: Font.HasDmlEffect
second_title: Aspose.Words für .NET-API-Referenz
description: Font methode. Überprüft ob ein bestimmter DrawingMLTexteffekt angewendet wird.
type: docs
weight: 560
url: /de/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Überprüft, ob ein bestimmter DrawingML-Texteffekt angewendet wird.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | DrawingML-Texteffekttyp. |

### Rückgabewert

True, wenn ein bestimmter DrawingML-Texteffekt angewendet wird.

### Beispiele

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

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


