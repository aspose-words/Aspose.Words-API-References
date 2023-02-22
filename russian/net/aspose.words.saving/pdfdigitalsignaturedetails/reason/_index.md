---
title: PdfDigitalSignatureDetails.Reason
second_title: Справочник по API Aspose.Words для .NET
description: PdfDigitalSignatureDetails свойство. Получает или задает причину подписания.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/pdfdigitalsignaturedetails/reason/
---
## PdfDigitalSignatureDetails.Reason property

Получает или задает причину подписания.

```csharp
public string Reason { get; set; }
```

### Примечания

Значение по умолчанию равно null.

### Примеры

Показывает, как подписать сгенерированный PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Настройте объект "DigitalSignatureDetails" объекта "SaveOptions" на
// подписать документ цифровой подписью, когда мы визуализируем его, с помощью метода «Сохранить».
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Смотрите также

* class [PdfDigitalSignatureDetails](../)
* пространство имен [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* сборка [Aspose.Words](../../../)


