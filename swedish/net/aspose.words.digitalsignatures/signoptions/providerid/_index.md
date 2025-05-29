---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SignOptions ProviderId, som definierar din signaturleverantörs klass-ID. Anpassa enkelt med ett unikt GUID för optimal prestanda.
type: docs
weight: 40
url: /sv/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Anger klass-ID för signaturleverantören. Standardvärdet är**Tom (bara nollor) Guid** .

```csharp
public Guid ProviderId { get; set; }
```

## Anmärkningar

Kryptografiska tjänsteleverantören (CSP) är en oberoende programmodul som faktiskt utför kryptografiska algoritmer för autentisering, kodning och kryptering. MS Office reserverar värdet {00000000-0000-0000-0000-00000000000} för sin standardsignaturleverantör.

GUID för den ytterligare installerade providern bör hämtas från dokumentationen som medföljde providern.

Dessutom listas alla installerade kryptografiska leverantörer i Windows-registret. Den finns på följande sökväg: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Det finns en nyckel med namnet "CP Service UUID" som motsvarar ett GUID för signaturleverantören.

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

* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
