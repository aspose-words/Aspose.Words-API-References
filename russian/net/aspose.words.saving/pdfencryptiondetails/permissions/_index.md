---
title: PdfEncryptionDetails.Permissions
linktitle: Permissions
articleTitle: Permissions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfEncryptionDetails Permissions, которое определяет операции пользователя с зашифрованными PDF-файлами. Разблокируйте безопасное управление документами с настраиваемым доступом!
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pdfencryptiondetails/permissions/
---
## PdfEncryptionDetails.Permissions property

Указывает операции, разрешенные пользователю для зашифрованного PDF-документа. Значение по умолчанию:DisallowAll .

```csharp
public PdfPermissions Permissions { get; set; }
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
