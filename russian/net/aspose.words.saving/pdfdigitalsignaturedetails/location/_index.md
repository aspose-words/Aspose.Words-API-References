---
title: PdfDigitalSignatureDetails.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfDigitalSignatureDetails Location, чтобы легко управлять и настраивать место подписания документов для повышения безопасности и эффективности.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pdfdigitalsignaturedetails/location/
---
## PdfDigitalSignatureDetails.Location property

Получает или задает место подписания.

```csharp
public string Location { get; set; }
```

## Примечания

Значение по умолчанию:`нулевой` .

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
