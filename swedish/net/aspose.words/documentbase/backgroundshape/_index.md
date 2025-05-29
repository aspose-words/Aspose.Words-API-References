---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DocumentBase BackgroundShape och anpassa enkelt dokumentets bakgrundsform för förbättrad visuell attraktionskraft. Maximera din designpotential!
type: docs
weight: 10
url: /sv/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Hämtar eller ställer in dokumentets bakgrundsform. Kan vara`null` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Anmärkningar

Microsoft Word tillåter endast en form som har sin[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) egenskapen lika med Rectangle att användas som bakgrundsform för ett dokument.

Microsoft Word stöder endast fyllningsegenskaperna för en bakgrundsform. Alla andra egenskaper ignoreras.

Om du anger ett värde som inte är null för den här egenskapen kommer även[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) till`sann`.

## Exempel

Visar hur man ställer in en bakgrundsform för varje sida i ett dokument.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Den enda formtypen vi kan använda som bakgrund är en rektangel.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Det finns två sätt att använda den här formen som bakgrund på sidan.
// 1 - En platt färg:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - En bild:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Justera bildens utseende för att göra den mer lämplig som vattenstämpel.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word stöder inte former med bilder som bakgrunder,
// men vi kan fortfarande se dessa bakgrunder i andra sparformat som .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
