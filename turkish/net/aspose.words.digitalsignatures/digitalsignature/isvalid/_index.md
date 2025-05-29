---
title: DigitalSignature.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: .NET için Aspose.Words
description: Belge bütünlüğünü DigitalSignature IsValid özelliğiyle güvence altına alın, özgünlüğü onaylayın ve kurcalamaya karşı koruma sağlayın. Dijital imzalarınıza güvenin!
type: docs
weight: 40
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Geri Döndürür`doğru` bu dijital imza geçerliyse ve belgede değişiklik yapılmamışsa.

```csharp
public bool IsValid { get; }
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
