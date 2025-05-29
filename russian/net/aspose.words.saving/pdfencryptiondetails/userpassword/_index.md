---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words для .NET
description: Узнайте, как свойство UserPassword повышает безопасность PDF-файлов, требуя пароль для доступа, гарантируя защиту и конфиденциальность ваших документов.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа.

```csharp
public string UserPassword { get; set; }
```

## Примечания

Для открытия зашифрованного PDF-документа для просмотра потребуется пароль пользователя. Разрешения, указанные в [`Permissions`](../permissions/) будет выполняться программным обеспечением считывателя.

Пароль пользователя может быть`нулевой` или пустая строка, в этом случае пароль не будет запрашиваться от пользователя при открытии документа PDF . Пароль пользователя не может совпадать с паролем владельца.

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

* class [PdfEncryptionDetails](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
