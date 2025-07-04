---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words for .NET
description: Discover if a specific DrawingML text effect is applied with the Font HasDmlEffect method. Enhance your document's visual appeal effortlessly!
type: docs
weight: 570
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

Assert.That(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow), Is.True);
Assert.That(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow), Is.True);
Assert.That(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection), Is.True);
Assert.That(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D), Is.True);
Assert.That(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill), Is.True);
```

### See Also

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
