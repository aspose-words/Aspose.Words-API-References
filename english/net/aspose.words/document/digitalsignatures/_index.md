---
title: Document.DigitalSignatures
linktitle: DigitalSignatures
articleTitle: DigitalSignatures
second_title: Aspose.Words for .NET
description: Discover the DigitalSignatures property to access and validate a document's digital signatures effortlessly. Ensure authenticity and security with ease.
type: docs
weight: 110
url: /net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Gets the collection of digital signatures for this document and their validation results.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

## Remarks

This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [`Document`](../) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never `null`. If the document is not signed, it will contain zero elements.

## Examples

Shows how to validate and display information about each signature in a document.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}");
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
