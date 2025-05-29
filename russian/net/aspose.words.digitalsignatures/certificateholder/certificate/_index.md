---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: Aspose.Words для .NET
description: Получите доступ к экземпляру X509Certificate2 с помощью закрытых ключей и цепочки сертификатов. Упростите управление безопасностью с помощью нашего свойства CertificateHolder.
type: docs
weight: 20
url: /ru/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

Возвращает экземпляр**X509Сертификат2** который содержит закрытые, открытые ключи и цепочку сертификатов.

```csharp
public X509Certificate2 Certificate { get; }
```

### Возвращаемое значение

X509Certificate2 пример

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

* class [CertificateHolder](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
