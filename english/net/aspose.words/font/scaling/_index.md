---
title: Font.Scaling
linktitle: Scaling
second_title: Aspose.Words for .NET API Reference
description: Font property. Gets or sets character width scaling in percent in C#.
type: docs
weight: 310
url: /net/aspose.words/font/scaling/
---
## Font.Scaling property

Gets or sets character width scaling in percent.

```csharp
public int Scaling { get; set; }
```

## Examples

Shows how to set horizontal scaling and spacing for characters.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add run of text and increase character width to 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Add run of text and add 1pt of extra horizontal spacing between each character.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Add run of text and bring characters closer together by 1pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
