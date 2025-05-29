---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen TextBox VerticalAnchor förbättrar textjusteringen i former för förbättrad design och läsbarhet i dina projekt.
type: docs
weight: 120
url: /sv/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Anger den vertikala justeringen av texten inom en form.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Anmärkningar

Standardvärdet ärTop.

## Exempel

Visar hur man justerar textinnehållet i en textruta vertikalt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" för att
// justera texten i den här textrutan med formens översida.
// Sätt egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" till
// justera texten i den här textrutan till formens mitt.
// Sätt egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" för att
// justera texten i den här textrutan mot formens nederkant.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Vertikal justering av text inuti textrutor är tillgänglig från och med Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Se även

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
