---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: .NET için Aspose.Words
description: İmzalama sürecinizi net amaçlı yorumlarla geliştirmek için DigitalSignature Yorumları özelliğini keşfedin. Belgelerinizdeki verimliliği ve netliği artırın!
type: docs
weight: 20
url: /tr/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

İmzalama amacı yorumunu alır.

```csharp
public string Comments { get; }
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
