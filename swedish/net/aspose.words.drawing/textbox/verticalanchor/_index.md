---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words för .NET
description: TextBox VerticalAnchor fast egendom. Anger den vertikala justeringen av texten inom en form i C#.
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

Visar hur man vertikalt justerar textinnehållet i en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" till
// justera texten i denna textruta med formens övre sida.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" till
// justera texten i denna textruta till mitten av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" till
// justera texten i den här textrutan till botten av formen.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Den vertikala justeringen av text inuti textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Se även

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
