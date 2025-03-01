---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words for .NET
description: Discover the Font Engrave property. Easily format fonts for an elegant engraved look, enhancing your design's sophistication and appeal.
type: docs
weight: 120
url: /net/aspose.words/font/engrave/
---
## Font.Engrave property

True if the font is formatted as engraved.

```csharp
public bool Engrave { get; set; }
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
