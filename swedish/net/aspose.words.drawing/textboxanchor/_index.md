---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.TextBoxAnchor-enum för exakt vertikal justering av formtext. Förbättra formateringen av ditt dokument utan ansträngning!
type: docs
weight: 1740
url: /sv/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Anger värden som används för vertikal justering av formtext.

```csharp
public enum TextBoxAnchor
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | `0` | Texten är justerad mot textrutans överkant. |
| Middle | `1` | Texten är justerad till mitten av textrutan. |
| Bottom | `2` | Texten är justerad längst ner i textrutan. |
| TopCentered | `3` | Texten är justerad till den övre delen av textrutan och centrerad. |
| MiddleCentered | `4` | Texten är justerad till mitten och centrerad i textrutan. |
| BottomCentered | `5` | Texten är justerad mot textrutans nederkant och centrerad. |
| TopBaseline | `6` | Texten är justerad mot textrutans övre baslinje. |
| BottomBaseline | `7` | Texten är justerad mot textrutans nedre baslinje. |
| TopCenteredBaseline | `8` | Texten är justerad mot den övre centrerade baslinjen i textrutan. |
| BottomCenteredBaseline | `9` | Texten är justerad mot den nedre centrerade baslinjen i textrutan. |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
