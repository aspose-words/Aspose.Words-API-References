---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words for .NET
description: Discover the Font TextEffect property to easily customize font animations, enhancing your designs with dynamic text effects for a captivating user experience.
type: docs
weight: 460
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
