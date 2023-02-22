---
title: TextEffect
second_title: Aspose.Words for .NET API Reference
description: Font property. Gets or sets the font animation effect in C#.
type: docs
weight: 450
url: /net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Gets or sets the font animation effect.

```csharp
public TextEffect TextEffect { get; set; }
```

## Examples

Shows how to apply a visual effect to a run.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Older versions of Microsoft Word only support font animation effects.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### See Also

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
