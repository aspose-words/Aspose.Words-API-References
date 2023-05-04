---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words for .NET
description: Font HasDmlEffect method. Checks if particular DrawingML text effect is applied in C#.
type: docs
weight: 560
url: /net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Checks if particular DrawingML text effect is applied.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | DrawingML text effect type. |

### Return Value

`true` if particular DrawingML text effect is applied.

## Examples

Shows how to check if a run displays a DrawingML text effect.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### See Also

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
