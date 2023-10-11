---
title: PdfEncryptionDetails.UserPassword
second_title: Справочник по API Aspose.Words для .NET
description: PdfEncryptionDetails свойство. Указывает пароль пользователя необходимый для открытия зашифрованного PDFдокумента.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа.

```csharp
public string UserPassword { get; set; }
```

### Примечания

Пароль пользователя потребуется для открытия зашифрованного PDF-документа для просмотра. Разрешения, указанные в [`Permissions`](../permissions/) будет обеспечиваться программным обеспечением считывателя.

Пароль пользователя может быть`нулевой` или пустая строка, в этом случае пароль от пользователя при открытии PDF-документа не потребуется. Пароль пользователя не может совпадать с паролем владельца.

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


