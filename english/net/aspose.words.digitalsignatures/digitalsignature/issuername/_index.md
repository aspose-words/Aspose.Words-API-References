---
title: DigitalSignature.IssuerName
linktitle: IssuerName
articleTitle: IssuerName
second_title: Aspose.Words for .NET
description: Discover the DigitalSignature IssuerName property, providing the issuer's distinguished name for enhanced security and trust in your digital certificates.
type: docs
weight: 30
url: /net/aspose.words.digitalsignatures/digitalsignature/issuername/
---
## DigitalSignature.IssuerName property

Returns the subject distinguished name of the certificate isuuer.

```csharp
public string IssuerName { get; }
```

## Examples

Shows how to sign documents with X.509 certificates.

```csharp
// Verify that a document is not signed.
Assert.That(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature, Is.False);

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.That(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature, Is.True);

// 2 - Take a document from a stream and save a signed copy to another stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.That(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature, Is.True);

// Please verify that all of the document's digital signatures are valid and check their details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.That(digitalSignatureCollection.IsValid, Is.True);
Assert.That(digitalSignatureCollection.Count, Is.EqualTo(1));
Assert.That(digitalSignatureCollection[0].SignatureType, Is.EqualTo(DigitalSignatureType.XmlDsig));
Assert.That(signedDoc.DigitalSignatures[0].IssuerName, Is.EqualTo("CN=Morzal.Me"));
Assert.That(signedDoc.DigitalSignatures[0].SubjectName, Is.EqualTo("CN=Morzal.Me"));
```

### See Also

* class [DigitalSignature](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
