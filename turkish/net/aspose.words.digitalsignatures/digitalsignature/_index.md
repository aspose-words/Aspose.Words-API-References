---
title: Class DigitalSignature
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DigitalSignatures.DigitalSignature sınıf. Bir belgedeki dijital imzayı ve doğrulamasının sonucunu temsil eder.
type: docs
weight: 380
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Bir belgedeki dijital imzayı ve doğrulamasının sonucunu temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışma](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokümantasyon makalesi.

```csharp
public class DigitalSignature
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | İmzalama amacı yorumunu alır. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Sertifikanın konu ayırt edici adını döndürür isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | İadeler`doğru` bu dijital imza geçerliyse ve belgeye müdahale edilmemişse. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Dijital imzanın türünü alır. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Bir imza değerini temsil eden bayt dizisini alır. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Belgenin imzalandığı zamanı alır. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adını döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür. |

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

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)


