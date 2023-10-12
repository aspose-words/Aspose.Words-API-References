---
title: SignatureLineOptions.ShowDate
second_title: Aspose.Words für .NET-API-Referenz
description: SignatureLineOptions eigendom. Ruft einen Wert ab oder legt diesen fest der angibt dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft istWAHR .
type: docs
weight: 60
url: /de/net/aspose.words/signaturelineoptions/showdate/
---
## SignatureLineOptions.ShowDate property

Ruft einen Wert ab oder legt diesen fest, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Der Standardwert für diese Eigenschaft ist`WAHR` .

```csharp
public bool ShowDate { get; set; }
```

### Beispiele

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

* class [SignatureLineOptions](../)
* namensraum [Aspose.Words](../../signaturelineoptions/)
* Montage [Aspose.Words](../../../)


