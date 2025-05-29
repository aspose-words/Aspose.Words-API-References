---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.SignatureLineOptions för att enkelt anpassa signaturrader i dina dokument. Förbättra din DocumentBuilder-upplevelse idag!
type: docs
weight: 6940
url: /sv/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Gör det möjligt att ange alternativ för signaturrad som infogas. Används i[`DocumentBuilder`](../documentbuilder/) .

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class SignatureLineOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Hämtar eller anger ett värde som anger att signeraren kan lägga till kommentarer i dialogrutan Signera. Standardvärdet för den här egenskapen är`falsk` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Hämtar eller anger ett värde som anger att standardinstruktioner visas i dialogrutan Signera. Standardvärdet för den här egenskapen är`sann` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Hämtar eller ställer in den föreslagna undertecknarens e-postadress. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Hämtar eller anger instruktioner till undertecknaren som visas vid signering av signaturraden. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Hämtar eller ställer in ett värde som anger att signeringsdatum visas på signaturraden. Standardvärdet för den här egenskapen är`sann` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Hämtar eller ställer in föreslagen undertecknare för signaturraden. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Hämtar eller ställer in föreslagen undertecknares titel. Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |

## Exempel

Visar hur man signerar ett dokument med ett personligt certifikat och en signaturrad.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Öppna vårt sparade dokument igen och verifiera att egenskaperna "IsSigned" och "IsValid" båda är lika med "true",
// indikerar att signaturraden innehåller en signatur.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
