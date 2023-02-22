---
title: SignatureLine.Signer
second_title: Aspose.Words för .NET API Referens
description: SignatureLine fast egendom. Hämtar eller ställer in föreslagen undertecknare av signaturraden. Standardvärdet för den här egenskapen är tom sträng Empty .
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/signatureline/signer/
---
## SignatureLine.Signer property

Hämtar eller ställer in föreslagen undertecknare av signaturraden. Standardvärdet för den här egenskapen är **tom sträng** (Empty ).

```csharp
public string Signer { get; set; }
```

### Exempel

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

// Infoga en form som kommer att innehålla en signaturlinje, vars utseende vi kommer att göra
// anpassa med "SignatureLineOptions"-objektet vi har skapat ovan.
// Om vi infogar en form vars koordinater kommer från det nedre högra hörnet på sidan,
// vi kommer att behöva ange negativa x- och y-koordinater för att få formen att synas.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Verifiera egenskaperna för vår signaturlinje via dess Shape-objekt.
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
* namnutrymme [Aspose.Words.Drawing](../../signatureline/)
* hopsättning [Aspose.Words](../../../)


