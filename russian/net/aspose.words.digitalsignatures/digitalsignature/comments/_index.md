---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DigitalSignature Comments, чтобы улучшить процесс подписания с помощью четких комментариев о цели. Повысьте эффективность и ясность в ваших документах!
type: docs
weight: 20
url: /ru/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

Получает комментарий цели подписи.

```csharp
public string Comments { get; }
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

* class [DigitalSignature](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
