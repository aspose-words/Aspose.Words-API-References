---
title: PdfSaveOptions.DigitalSignatureDetails
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает данные для подписи выходного PDFдокумента.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Получает или задает данные для подписи выходного PDF-документа.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

### Примечания

Значение по умолчанию:`нулевой`и выходной документ не будет подписан. Если для этого свойства установлено допустимое значение[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, , то выходной PDF-документ будет иметь цифровую подпись.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


