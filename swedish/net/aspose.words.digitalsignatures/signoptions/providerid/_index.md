---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words för .NET
description: SignOptions ProviderId fast egendom. Anger klassID för signaturleverantören. Standardvärdet ärTom alla nollor Guid  i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Anger klass-ID för signaturleverantören. Standardvärdet är**Tom (alla nollor) Guid** .

```csharp
public Guid ProviderId { get; set; }
```

## Anmärkningar

Den kryptografiska tjänsteleverantören (CSP) är en oberoende programvarumodul som faktiskt utför kryptografialgoritmer för autentisering, kodning och kryptering. MS Office reserverar värdet av {00000000-0000-0000-0000-0000000000000} för sin standardsignaturleverantör.

GUID för den extra installerade leverantören bör erhållas från dokumentationen som levereras med leverantören.

Dessutom är alla installerade kryptografiska leverantörer uppräknade i Windows-registret. Den kan hittas i följande sökväg: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Det finns ett nyckelnamn "CP Service UUID" som motsvarar en GUID för signaturleverantör.

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

* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
