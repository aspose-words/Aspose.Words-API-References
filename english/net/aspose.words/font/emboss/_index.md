---
title: Font.Emboss
linktitle: Emboss
second_title: Aspose.Words for .NET API Reference
description: Font Emboss property. True if the font is formatted as embossed in C#.
type: docs
weight: 100
url: /net/aspose.words/font/emboss/
---
## Emboss property

True if the font is formatted as embossed.

```csharp
public bool Emboss { get; set; }
```

## Examples

Shows how to apply engraving/embossing effects to text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Below are two ways of using shadows to apply a 3D-like effect to the text.
// 1 -  Engrave text to make it look like the letters are sunken into the page:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 -  Emboss text to make it look like the letters pop out of the page:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
