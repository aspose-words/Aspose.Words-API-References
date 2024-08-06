---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words for .NET
description: Aspose.Words.TextDmlEffect enum. Dml text effect for text runs in C#.
type: docs
weight: 6770
url: /net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Dml text effect for text runs.

```csharp
public enum TextDmlEffect
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Glow | `0` | Glow effect, in which a color blurred outline is added outside the edges of the object. |
| Fill | `1` | Fill overlay effect. |
| Shadow | `2` | Shadow effect. |
| Outline | `3` | Outline effect. |
| Effect3D | `4` | 3D effect. |
| Reflection | `5` | Reflection effect. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
