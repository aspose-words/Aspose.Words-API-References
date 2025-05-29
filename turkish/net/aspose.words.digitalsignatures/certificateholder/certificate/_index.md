---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: .NET için Aspose.Words
description: Özel anahtarlar ve sertifika zinciriyle X509Certificate2 örneğine erişin. CertificateHolder özelliğimizle güvenlik yönetiminizi basitleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

örneğini döndürür**X509Sertifika2** özel, genel anahtarları ve sertifika zincirini tutan.

```csharp
public X509Certificate2 Certificate { get; }
```

### Geri dönüş değeri

X509Certificate2 misal

## Örnekler

Bir belgedeki her imzaya ilişkin bilgilerin nasıl doğrulanacağını ve görüntüleneceğini gösterir.

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

* class [CertificateHolder](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
