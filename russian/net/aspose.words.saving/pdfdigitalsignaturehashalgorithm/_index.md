---
title: Enum PdfDigitalSignatureHashAlgorithm
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm перечисление. Указывает цифровой алгоритм хеширования используемый цифровой подписью.
type: docs
weight: 5440
url: /ru/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Указывает цифровой алгоритм хеширования, используемый цифровой подписью.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Sha256 | `0` | Алгоритм хеширования SHA-256. |
| Sha384 | `1` | Алгоритм хеширования SHA-384. |
| Sha512 | `2` | Алгоритм хеширования SHA-512. |
| RipeMD160 | `3` | Алгоритм хеширования RIPEMD-160. |

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


