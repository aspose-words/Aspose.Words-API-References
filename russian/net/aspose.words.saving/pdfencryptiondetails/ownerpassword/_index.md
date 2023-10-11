---
title: PdfEncryptionDetails.OwnerPassword
second_title: Справочник по API Aspose.Words для .NET
description: PdfEncryptionDetails свойство. Указывает пароль владельца для зашифрованного PDFдокумента.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Указывает пароль владельца для зашифрованного PDF-документа.

```csharp
public string OwnerPassword { get; set; }
```

### Примечания

Пароль владельца позволяет пользователю открывать зашифрованный PDF-документ без каких-либо ограничений доступа , указанных в[`Permissions`](../permissions/).

Пароль владельца не может совпадать с паролем пользователя.

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

* class [PdfEncryptionDetails](../)
* пространство имен [Aspose.Words.Saving](../../pdfencryptiondetails/)
* сборка [Aspose.Words](../../../)


