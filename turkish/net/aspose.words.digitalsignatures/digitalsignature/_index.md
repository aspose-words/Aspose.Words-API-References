---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: .NET için Aspose.Words
description: Güvenli belge imzalama ve doğrulama için Aspose.Words.DigitalSignatures.DigitalSignature sınıfını keşfedin. Belge güvenliğinizi zahmetsizce artırın!
type: docs
weight: 580
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Bir belgedeki dijital imzayı ve doğrulamasının sonucunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class DigitalSignature
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | İmzalama amacı yorumunu alır. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Sertifikayı verenin konu ayırt edici adını döndürür. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Geri Döndürür`doğru` bu dijital imza geçerliyse ve belgede değişiklik yapılmamışsa. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Dijital imzanın türünü alır. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Bir imza değerini temsil eden bir bayt dizisi alır. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Belgenin imzalandığı zamanı alır. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adını döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür. |

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

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
