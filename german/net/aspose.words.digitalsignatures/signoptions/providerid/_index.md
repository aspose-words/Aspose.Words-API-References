---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words für .NET
description: Entdecken Sie die SignOptions ProviderId-Eigenschaft, die die Klassen-ID Ihres Signaturanbieters definiert. Für optimale Leistung können Sie die Eigenschaft ganz einfach mit einer eindeutigen GUID anpassen.
type: docs
weight: 40
url: /de/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Gibt die Klassen-ID des Signaturanbieters an. Der Standardwert ist**Leere (nur Nullen) GUID** .

```csharp
public Guid ProviderId { get; set; }
```

## Bemerkungen

Der Kryptografiedienstanbieter (CSP) ist ein unabhängiges Softwaremodul, das tatsächlich Kryptografiealgorithmen zur Authentifizierung, Verschlüsselung und Verschlüsselung ausführt. MS Office reserviert den Wert von {00000000-0000-0000-0000-000000000000} für seinen Standardsignaturanbieter.

Die GUID des zusätzlich installierten Providers entnehmen Sie bitte der mit dem Provider mitgelieferten Dokumentation.

Darüber hinaus werden alle installierten Kryptografieanbieter in der Windows-Registrierung aufgelistet. Sie befinden sich im folgenden Pfad: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Es gibt einen Schlüsselnamen „CP Service UUID“, der einer GUID des Signaturanbieters entspricht.

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

* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
