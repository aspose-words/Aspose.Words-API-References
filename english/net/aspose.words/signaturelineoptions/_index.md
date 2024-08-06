---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.SignatureLineOptions class. Allows to specify options for signature line being inserted. Used in DocumentBuilder in C#.
type: docs
weight: 6450
url: /net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Allows to specify options for signature line being inserted. Used in [`DocumentBuilder`](../documentbuilder/).

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class SignatureLineOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is `false`. |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is `true`. |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Gets or sets suggested signer's e-mail address. Default value for this property is **empty string** (Empty). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Gets or sets instructions to the signer that are displayed on signing the signature line. Default value for this property is **empty string** (Empty). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is `true`. |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Gets or sets suggested signer of the signature line. Default value for this property is **empty string** (Empty). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Gets or sets suggested signer's title. Default value for this property is **empty string** (Empty). |

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

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
