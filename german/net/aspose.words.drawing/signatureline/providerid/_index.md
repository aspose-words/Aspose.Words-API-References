---
title: SignatureLine.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words für .NET
description: SignatureLine ProviderId eigendom. Ruft die SignaturanbieterID für diese Signaturzeile ab oder legt sie fest. Der Standardwert ist 00000000000000000000000000000000 in C#.
type: docs
weight: 80
url: /de/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

Ruft die Signaturanbieter-ID für diese Signaturzeile ab oder legt sie fest. Der Standardwert ist „{00000000-0000-0000-0000-000000000000}“.

```csharp
public Guid ProviderId { get; set; }
```

## Bemerkungen

Der Kryptografiedienstanbieter (CSP) ist ein unabhängiges Softwaremodul, das tatsächlich Kryptografiealgorithmen zur Authentifizierung, Kodierung und Verschlüsselung ausführt. MS Office reserviert den Wert von {00000000-0000-0000-0000-000000000000} für seinen Standardsignaturanbieter.

Die GUID des zusätzlich installierten Providers entnehmen Sie bitte der mitgelieferten Dokumentation des Providers.

Darüber hinaus werden alle installierten Kryptografieanbieter in der Windows-Registrierung aufgelistet. Sie finden sie im folgenden Pfad: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Es gibt einen Schlüsselnamen „CP Service UUID“, der entspricht eine GUID des Signaturanbieters.

## Beispiele

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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

// Öffnen Sie unser gespeichertes Dokument erneut und überprüfen Sie, ob die Eigenschaften „IsSigned“ und „IsValid“ beide den Wert „true“ haben.
// zeigt an, dass die Signaturzeile eine Signatur enthält.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Siehe auch

* class [SignatureLine](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
