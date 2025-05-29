---
title: DigitalSignature.SignatureType
linktitle: SignatureType
articleTitle: SignatureType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DigitalSignature SignatureType, чтобы легко определить тип вашей цифровой подписи и повысить безопасность ваших документов уже сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

Получает тип цифровой подписи.

```csharp
public DigitalSignatureType SignatureType { get; }
```

## Примеры

Показывает, как проверять и отображать информацию о каждой подписи в документе.

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

### Смотрите также

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
