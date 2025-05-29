---
title: DigitalSignature.SignatureType
linktitle: SignatureType
articleTitle: SignatureType
second_title: .NET için Aspose.Words
description: Dijital imza türünüzü kolayca belirlemek ve belge güvenliğinizi artırmak için DigitalSignature SignatureType özelliğini keşfedin!
type: docs
weight: 50
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

Dijital imzanın türünü alır.

```csharp
public DigitalSignatureType SignatureType { get; }
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

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
