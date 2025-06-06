---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TextBox InternalMarginTop – styr din formes övre marginal i punkter för exakt layout och förbättrad designflexibilitet.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Anger den inre övre marginalen i punkter för en form.

```csharp
public double InternalMarginTop { get; set; }
```

## Anmärkningar

Standardvärdet är 1/20 tum.

## Exempel

Visar hur man ställer in interna marginaler för en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ytterligare en textruta med specifika marginaler.
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
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
