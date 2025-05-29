---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words для .NET
description: Откройте для себя свойство EncryptionDetails в PdfSaveOptions, чтобы легко настроить параметры шифрования PDF-файлов, гарантируя безопасность и защищенность ваших документов.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

Возвращает или задает параметры шифрования выходного PDF-документа.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## Примечания

Значение по умолчанию:`нулевой` и выходной документ не будет зашифрован. Когда это свойство установлено в допустимое значение[`PdfEncryptionDetails`](../../pdfencryptiondetails/)object, , то выходной PDF-документ будет зашифрован.

При сохранении в формате PDF 1.7 (включая PDF/UA-1) используется алгоритм шифрования AES-128. При сохранении в формате PDF 2.0 используется алгоритм шифрования AES-256.

Шифрование запрещено соответствием PDF/A. Эта опция будет проигнорирована при сохранении в PDF/A.

ContentCopyForAccessibility требуется разрешение PDF/UA compliance , если выходной документ зашифрован. Это разрешение будет автоматически использоваться при сохранении в PDF/UA.

ContentCopyForAccessibility разрешение устарело в формате PDF 2.0. Это разрешение будет проигнорировано при сохранении в формате PDF 2.0.

## Примеры

Показывает, как установить разрешения для сохраненного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Расширить разрешения, чтобы разрешить редактирование аннотаций.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Включить шифрование через свойство «EncryptionDetails».
saveOptions.EncryptionDetails = encryptionDetails;

// Когда мы откроем этот документ, нам нужно будет указать пароль, прежде чем получить доступ к его содержимому.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### Смотрите также

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
