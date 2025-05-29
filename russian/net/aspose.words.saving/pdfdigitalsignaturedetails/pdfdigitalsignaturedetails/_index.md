---
title: PdfDigitalSignatureDetails
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор PdfDigitalSignatureDetails, предназначенный для эффективной инициализации экземпляров цифровой подписи для безопасного управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pdfdigitalsignaturedetails/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails() {#constructor}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureDetails()
```

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

* class [PdfDigitalSignatureDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PdfDigitalSignatureDetails(*[CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) {#constructor_1}

Инициализирует экземпляр этого класса.

```csharp
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, string reason, 
    string location, DateTime signatureDate)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| certificateHolder | CertificateHolder | Держатель сертификата, содержащий сам сертификат. |
| reason | String | Причина подписания. |
| location | String | Место подписания. |
| signatureDate | DateTime | Дата и время подписания. |

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [PdfDigitalSignatureDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
