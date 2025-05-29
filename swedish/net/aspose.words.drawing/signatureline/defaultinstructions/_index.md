---
title: SignatureLine.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SignatureLine DefaultInstructions förbättrar din signeringsdialogruta med anpassningsbara standardinstruktioner för en sömlös användarupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/signatureline/defaultinstructions/
---
## SignatureLine.DefaultInstructions property

Hämtar eller anger ett värde som anger att standardinstruktioner visas i dialogrutan Signera. Standardvärdet för den här egenskapen är`sann` .

```csharp
public bool DefaultInstructions { get; set; }
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

* class [SignatureLine](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
