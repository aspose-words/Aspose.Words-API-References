---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.DigitalSignatures.DigitalSignature class. Represents a digital signature on a document and the result of its verification in C#.
type: docs
weight: 370
url: /net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Represents a digital signature on a document and the result of its verification.

To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/net/working-with-digital-signatures/) documentation article.

```csharp
public class DigitalSignature
```

## Properties

| Name | Description |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Gets the signing purpose comment. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Returns the subject distinguished name of the certificate isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Returns `true` if this digital signature is valid and the document has not been tampered with. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Gets the type of the digital signature. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Gets the time the document was signed. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Returns the subject distinguished name of the certificate that was used to sign the document. |

## Methods

| Name | Description |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Returns a user-friendly string that displays the value of this object. |

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

### See Also

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
