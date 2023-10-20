---
title: SignatureLineOptions.AllowComments
linktitle: AllowComments
articleTitle: AllowComments
second_title: Aspose.Words för .NET
description: SignatureLineOptions AllowComments fast egendom. Hämtar eller ställer in ett värde som anger att undertecknaren kan lägga till kommentarer i dialogrutan Signera. Standardvärdet för den här egenskapen ärfalsk  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/signaturelineoptions/allowcomments/
---
## SignatureLineOptions.AllowComments property

Hämtar eller ställer in ett värde som anger att undertecknaren kan lägga till kommentarer i dialogrutan Signera. Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool AllowComments { get; set; }
```

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

// Öppna vårt sparade dokument igen och kontrollera att egenskaperna "IsSigned" och "IsValid" båda är lika med "true",
// indikerar att signaturraden innehåller en signatur.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Se även

* class [SignatureLineOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
