---
title: SignatureLine.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words for .NET
description: Ensure your documents are secure with SignatureLine's IsValid property, confirming valid digital signatures for authenticity and trust.
type: docs
weight: 70
url: /net/aspose.words.drawing/signatureline/isvalid/
---
## SignatureLine.IsValid property

Indicates that signature line is signed by digital signature and this digital signature is valid.

```csharp
public bool IsValid { get; }
```

## Examples

Shows how to sign a document with a personal certificate and a signature line.

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

Assert.That(signatureLine.IsSigned, Is.False);
Assert.That(signatureLine.IsValid, Is.False);

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

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.That(signatureLine.IsSigned, Is.True);
Assert.That(signatureLine.IsValid, Is.True);
```

### See Also

* class [SignatureLine](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
