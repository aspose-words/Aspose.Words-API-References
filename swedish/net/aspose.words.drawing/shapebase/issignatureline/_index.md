---
title: ShapeBase.IsSignatureLine
linktitle: IsSignatureLine
articleTitle: IsSignatureLine
second_title: Aspose.Words för .NET
description: Upptäck ShapeBases IsSignatureLine-egenskap, som definierar former som SignatureLines, vilket förbättrar dokumentintegriteten och den professionella presentationen.
type: docs
weight: 360
url: /sv/net/aspose.words.drawing/shapebase/issignatureline/
---
## ShapeBase.IsSignatureLine property

Indikerar att formen är en[`SignatureLine`](../../signatureline/) .

```csharp
public bool IsSignatureLine { get; }
```

## Exempel

Visar hur man skapar en rad för en signatur och infogar den i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Infoga en form som ska innehålla en signaturrad, vars utseende vi kommer att
// anpassa med hjälp av objektet "SignatureLineOptions" som vi skapade ovan.
// Om vi infogar en form vars koordinater har sitt ursprung i sidans nedre högra hörn,
// vi måste ange negativa x- och y-koordinater för att få formen att synas.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifiera egenskaperna för vår signaturrad via dess Shape-objekt.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
