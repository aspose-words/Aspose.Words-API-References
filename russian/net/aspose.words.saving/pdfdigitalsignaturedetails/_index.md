---
title: Class PdfDigitalSignatureDetails
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.PdfDigitalSignatureDetails сорт. Содержит сведения о подписании PDFдокумента цифровой подписью.
type: docs
weight: 5430
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
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(CertificateHolder, string, string, DateTime) | Инициализирует экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Возвращает объект владельца сертификата, содержащий сертификат, использованный для подписи документа. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Получает или задает алгоритм хеширования. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Получает или задает местоположение подписи. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Получает или задает причину подписи. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Получает или задает дату подписания. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Получает или задает настройки отметки времени цифровой подписи. |

### Примечания

На данный момент цифровая подпись документов PDF доступна только в .NET 2.0 или более поздней версии.

Чтобы поставить цифровую подпись PDF-документу при его создании в Aspose.Words, установите[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) свойство в допустимое`PdfDigitalSignatureDetails` объект, а затем сохраните документ в формате PDF, передав [`PdfSaveOptions`](../pdfsaveoptions/) в качестве параметра в[`Save`](../../aspose.words/document/save/) метод.

Aspose.Words создает подпись PKCS#7 для всего PDF-документа и использует фильтр «Adobe.PPKMS» и подфильтр «adbe.pkcs7.sha1» при создании цифровой подписи.

### Примеры

Показывает, как подписать созданный PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Настройте объект «DigitalSignatureDetails» объекта «SaveOptions» для
// снабжаем документ цифровой подписью при его рендеринге с помощью метода «Сохранить».
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


