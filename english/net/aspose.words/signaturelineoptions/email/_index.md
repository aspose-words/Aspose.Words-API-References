---
title: SignatureLineOptions.Email
linktitle: Email
articleTitle: Email
second_title: Aspose.Words for .NET
description: Manage suggested signer email addresses effortlessly with SignatureLineOptions. Enhance your email workflow with customizable options for seamless communication.
type: docs
weight: 40
url: /net/aspose.words/signaturelineoptions/email/
---
## SignatureLineOptions.Email property

Gets or sets suggested signer's e-mail address. Default value for this property is **empty string** (Empty).

```csharp
public string Email { get; set; }
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

* class [SignatureLineOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
