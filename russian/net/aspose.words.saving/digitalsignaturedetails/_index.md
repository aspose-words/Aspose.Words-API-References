---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.DigitalSignatureDetails для бесшовной цифровой подписи документов. Повысьте безопасность и подлинность без усилий!
type: docs
weight: 5640
url: /ru/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

Содержит данные для подписания документа цифровой подписью.

```csharp
public class DigitalSignatureDetails
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | Инициализирует новый экземпляр`DigitalSignatureDetails` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | Получает или задает[`CertificateHolder`](./certificateholder/) объект, содержащий сертификат, используемый для подписи документа. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | Получает или задает[`SignOptions`](./signoptions/) объект, используемый для подписи документа. |

## Примеры

Показывает, как подписывать документ OOXML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(
    certificateHolder,
    new SignOptions() { Comments = "Some comments", SignTime = DateTime.Now });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
