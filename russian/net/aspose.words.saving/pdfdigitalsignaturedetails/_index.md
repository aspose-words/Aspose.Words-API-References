---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.PdfDigitalSignatureDetails для бесшовной цифровой подписи PDF. Повысьте безопасность документов с помощью простой интеграции и надежных функций.
type: docs
weight: 6220
url: /ru/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Содержит сведения о подписании PDF-документа цифровой подписью.

```csharp
public class PdfDigitalSignatureDetails
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Инициализирует экземпляр этого класса. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Инициализирует экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Возвращает объект владельца сертификата, содержащий сертификат, который использовался для подписи документа. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Получает или задает алгоритм хэширования. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Получает или задает место подписания. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Получает или задает причину подписания. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Получает или задает дату подписания. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Получает или задает параметры временной метки цифровой подписи. |

## Примечания

В настоящее время цифровая подпись PDF-документов доступна только в .NET 3.5 и выше.

Чтобы подписать PDF-документ цифровой подписью при его создании с помощью Aspose.Words, установите[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) свойство к допустимому`PdfDigitalSignatureDetails` объект, а затем сохраните документ в формате PDF, передав [`PdfSaveOptions`](../pdfsaveoptions/) как параметр в[`Save`](../../aspose.words/document/save/) метод.

Aspose.Words создает подпись PKCS#7 для всего документа PDF и использует фильтр «Adobe.PPKMS» и подфильтр «adbe.pkcs7.sha1» при создании цифровой подписи.

## Примеры

Показывает, как подписать созданный PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Настройте объект "DigitalSignatureDetails" объекта "SaveOptions" для
// подписываем документ цифровой подписью, когда мы его отображаем с помощью метода «Сохранить».
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
