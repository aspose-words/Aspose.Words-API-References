---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.SignatureLine för att enkelt hantera och anpassa egenskaper för signaturrader för förbättrad dokumentsäkerhet.
type: docs
weight: 1700
url: /sv/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Ger åtkomst till egenskaper för signaturraden.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class SignatureLine
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Hämtar eller anger ett värde som anger att signeraren kan lägga till kommentarer i dialogrutan Signera. Standardvärdet för den här egenskapen är`falsk` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Hämtar eller anger ett värde som anger att standardinstruktioner visas i dialogrutan Signera. Standardvärdet för den här egenskapen är`sann` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Hämtar eller ställer in den föreslagna undertecknarens e-postadress. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Hämtar eller ställer in identifierare för denna signaturrad. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Hämtar eller anger instruktioner till undertecknaren som visas vid signering av signaturraden. Den här egenskapen ignoreras om[`DefaultInstructions`](./defaultinstructions/) är inställd. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Indikerar att signaturraden är signerad med digital signatur. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Indikerar att signaturraden är signerad med en digital signatur och att denna digitala signatur är giltig. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Hämtar eller ställer in signaturleverantörsidentifierare för denna signaturrad. Standardvärdet är "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Hämtar eller ställer in ett värde som anger att signeringsdatum visas på signaturraden. Standardvärdet för den här egenskapen är`sann` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Hämtar eller ställer in föreslagen undertecknare för signaturraden. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Hämtar eller ställer in föreslagen signerarens titel (till exempel Chef). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
