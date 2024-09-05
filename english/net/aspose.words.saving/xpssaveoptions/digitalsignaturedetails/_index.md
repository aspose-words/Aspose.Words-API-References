---
title: XpsSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words for .NET
description: XpsSaveOptions DigitalSignatureDetails property. Gets or sets DigitalSignatureDetails object used to sign a document in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/xpssaveoptions/digitalsignaturedetails/
---
## XpsSaveOptions.DigitalSignatureDetails property

Gets or sets [`DigitalSignatureDetails`](../../digitalsignaturedetails/) object used to sign a document.

```csharp
public DigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Examples

Shows how to sign XPS document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions options = new SignOptions();
options.SignTime = DateTime.Now;
options.Comments = "Some comments";

DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(certificateHolder, options);

XpsSaveOptions saveOptions = new XpsSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "XpsSaveOptions.XpsDigitalSignature.docx", saveOptions);
```

### See Also

* class [DigitalSignatureDetails](../../digitalsignaturedetails/)
* class [XpsSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
