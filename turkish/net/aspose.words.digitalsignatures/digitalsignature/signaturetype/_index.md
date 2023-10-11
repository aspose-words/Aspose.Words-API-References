---
title: DigitalSignature.SignatureType
second_title: Aspose.Words for .NET API Referansı
description: DigitalSignature mülk. Dijital imzanın türünü alır.
type: docs
weight: 50
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

Dijital imzanın türünü alır.

```csharp
public DigitalSignatureType SignatureType { get; }
```

### Örnekler

Bir belgedeki her imza hakkındaki bilgilerin nasıl doğrulanacağını ve görüntüleneceğini gösterir.

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

### Ayrıca bakınız

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* toplantı [Aspose.Words](../../../)


