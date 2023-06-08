---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words for .NET
description: Font Spacing property. Returns or sets the spacing in points between characters  in C#.
type: docs
weight: 380
url: /net/aspose.words/font/spacing/
---
## Font.Spacing property

Returns or sets the spacing (in points) between characters .

```csharp
public double Spacing { get; set; }
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
