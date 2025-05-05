---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.TextEffect enum for dynamic text animations. Enhance your documents with engaging effects for a captivating user experience.
type: docs
weight: 7270
url: /net/aspose.words/texteffect/
---
## TextEffect enumeration

Animation effect for text runs.

```csharp
public enum TextEffect
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
