---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор PdfEncryptionDetails для легкой инициализации защищенных экземпляров шифрования PDF. Улучшите защиту вашего документа с помощью нашего мощного инструмента!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

Инициализирует экземпляр этого класса.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### Смотрите также

* class [PdfEncryptionDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

Инициализирует экземпляр этого класса.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
```

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
