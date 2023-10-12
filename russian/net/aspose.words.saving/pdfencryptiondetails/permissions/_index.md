---
title: PdfEncryptionDetails.Permissions
second_title: Справочник по API Aspose.Words для .NET
description: PdfEncryptionDetails свойство. Указывает операции которые разрешены пользователю с зашифрованным PDFдокументом. Значение по умолчаниюDisallowAll .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Указывает операции, которые разрешены пользователю с зашифрованным PDF-документом. Значение по умолчанию:DisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
```

### Примеры

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* пространство имен [Aspose.Words.Saving](../../pdfencryptiondetails/)
* сборка [Aspose.Words](../../../)


