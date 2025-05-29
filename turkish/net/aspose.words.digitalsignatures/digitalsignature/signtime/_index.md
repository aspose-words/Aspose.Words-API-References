---
title: DigitalSignature.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: .NET için Aspose.Words
description: DigitalSignature SignTime'ı keşfedin. Gelişmiş güvenlik ve verimli kayıt tutma için belgelerinizin imzalandığı tam zamanı takip edin.
type: docs
weight: 70
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/signtime/
---
## DigitalSignature.SignTime property

Belgenin imzalandığı zamanı alır.

```csharp
public DateTime SignTime { get; }
```

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

* class [DigitalSignature](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
