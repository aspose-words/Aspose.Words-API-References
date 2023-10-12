---
title: DigitalSignature.IsValid
second_title: Aspose.Words for .NET API Referansı
description: DigitalSignature mülk. İadelerdoğru bu dijital imza geçerliyse ve belgeye müdahale edilmemişse.
type: docs
weight: 40
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

İadeler`doğru` bu dijital imza geçerliyse ve belgeye müdahale edilmemişse.

```csharp
public bool IsValid { get; }
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

* class [DigitalSignature](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* toplantı [Aspose.Words](../../../)


