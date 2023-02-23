---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.DigitalSignatures.DigitalSignatureCollection class. Provides a readonly collection of digital signatures attached to a document in C#.
type: docs
weight: 380
url: /net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Provides a read-only collection of digital signatures attached to a document.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## Constructors

| Name | Description |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Returns `true` if all digital signatures in this collection are valid and the document has not been tampered with Also returns `true` if there are no digital signatures. Returns `false` if at least one digital signature is invalid. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Gets a document signature at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Returns a dictionary enumerator object that can be used to iterate over all items in the collection. |

## Remarks

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

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
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Take a document from a stream and save a signed copy to another stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Please verify that all of the document's digital signatures are valid and check their details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### See Also

* class [DigitalSignature](../digitalsignature/)
* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
