---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: Discover the Font Shading property, which provides a Shading object for customizable font formatting, enhancing your text's visual appeal.
type: docs
weight: 330
url: /net/aspose.words/font/shading/
---
## Font.Shading property

Returns a [`Shading`](../../shading/) object that refers to the shading formatting for the font.

```csharp
public Shading Shading { get; }
```

## Examples

Shows how to apply shading to text created by a document builder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// One way to make the text created using our white font color visible
// is to apply a background shading effect.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### See Also

* class [Shading](../../shading/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
