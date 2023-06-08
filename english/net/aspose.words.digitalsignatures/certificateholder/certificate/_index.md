---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: Aspose.Words for .NET
description: CertificateHolder Certificate property. Returns the instance of X509Certificate2 which holds private public keys and certificate chain in C#.
type: docs
weight: 20
url: /net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

Returns the instance of **X509Certificate2** which holds private, public keys and certificate chain.

```csharp
public X509Certificate2 Certificate { get; }
```

### Return Value

X509Certificate2 instance

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

* class [CertificateHolder](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
