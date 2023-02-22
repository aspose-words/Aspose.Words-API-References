---
title: TextBox.InternalMarginRight
second_title: Aspose.Words för .NET API Referens
description: TextBox fast egendom. Anger den inre högra marginalen i punkter för en form.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Anger den inre högra marginalen i punkter för en form.

```csharp
public double InternalMarginRight { get; set; }
```

### Anmärkningar

Standardvärdet är 1/10 tum.

### Exempel

Visar hur man ställer in interna marginaler för en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en annan textruta med specifika marginaler.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Se även

* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../textbox/)
* hopsättning [Aspose.Words](../../../)


