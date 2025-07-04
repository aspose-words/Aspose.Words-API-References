---
title: DigitalSignatureType Enum
linktitle: DigitalSignatureType
articleTitle: DigitalSignatureType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.DigitalSignatures.DigitalSignatureType enum to enhance your document security with versatile digital signature options.
type: docs
weight: 590
url: /net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

Specifies the type of a digital signature.

```csharp
public enum DigitalSignatureType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | `0` | Indicates an error, unknown digital signature type. |
| CryptoApi | `1` | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| XmlDsig | `2` | The XmlDsig signature method used in OOXML and OpenDocument documents. |

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

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
