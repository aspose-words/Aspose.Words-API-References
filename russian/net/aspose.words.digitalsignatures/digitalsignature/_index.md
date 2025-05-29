---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DigitalSignatures.DigitalSignature для безопасной подписи и проверки документов. Повысьте безопасность своих документов без усилий!
type: docs
weight: 580
url: /ru/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Представляет цифровую подпись на документе и результат ее проверки.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public class DigitalSignature
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Возвращает объект владельца сертификата, содержащий сертификат, который использовался для подписи документа. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Получает комментарий цели подписи. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Возвращает отличительное имя субъекта сертификата isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Возврат`истинный` если эта цифровая подпись действительна и документ не был подделан. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Получает тип цифровой подписи. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Получает массив байтов, представляющих значение подписи. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Получает время подписания документа. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Возвращает отличительное имя субъекта сертификата, который использовался для подписи документа. |

## Методы

| Имя | Описание |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |

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

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
