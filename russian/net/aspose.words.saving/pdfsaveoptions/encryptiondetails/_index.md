---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words для .NET
description: PdfSaveOptions EncryptionDetails свойство. Получает или задает сведения для шифрования выходного PDFдокумента на С#.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Получает или задает сведения для шифрования выходного PDF-документа.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Примечания

Значение по умолчанию:`нулевой` и выходной документ не будет зашифрован. Если для этого свойства установлено допустимое значение[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, , то выходной PDF-документ будет зашифрован.

Алгоритм шифрования AES-128 используется при сохранении в формате PDF 1.7 (включая PDF/UA-1). Алгоритм шифрования AES-256 используется при сохранении в формате PDF 2.0.

Шифрование запрещено стандартом PDF/A. Эта опция будет игнорироваться при сохранении в PDF/A.

ContentCopyForAccessibility разрешение требуется PDF/UA Compliance , если выходной документ зашифрован. Это разрешение будет автоматически использовано при сохранении в PDF/UA.

ContentCopyForAccessibility разрешение устарело в формате PDF 2.0. Это разрешение будет игнорироваться при сохранении в PDF 2.0.

## Примеры

Показывает, как установить разрешения для сохраненного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Расширяем разрешения, чтобы разрешить редактирование аннотаций.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Включаем шифрование через свойство EncryptionDetails.
saveOptions.EncryptionDetails = encryptionDetails;

// Когда мы откроем этот документ, нам нужно будет ввести пароль, прежде чем получить доступ к его содержимому.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Смотрите также

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
