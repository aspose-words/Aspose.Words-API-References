---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: Aspose.Words для .NET
description: Узнайте, как свойство OwnerPassword защищает ваши зашифрованные файлы PDF, гарантируя только авторизованный доступ. Защитите свои документы без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

Указывает пароль владельца для зашифрованного PDF-документа.

```csharp
public string OwnerPassword { get; set; }
```

## Примечания

Пароль владельца позволяет пользователю открывать зашифрованный PDF-документ без каких-либо ограничений доступа , указанных в[`Permissions`](../permissions/).

Пароль владельца не может совпадать с паролем пользователя.

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
