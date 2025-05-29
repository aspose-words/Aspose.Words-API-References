---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.PdfEncryptionDetails для безопасного шифрования PDF-файлов и настраиваемых прав доступа, которые гарантируют защиту ваших документов.
type: docs
weight: 6250
url: /ru/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

Содержит сведения о шифровании и разрешениях доступа для PDF-документа.

Чтобы узнать больше, посетите[Защитить или зашифровать документ](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) документальная статья.

```csharp
public class PdfEncryptionDetails
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | Инициализирует экземпляр этого класса. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | Инициализирует экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | Указывает пароль владельца для зашифрованного PDF-документа. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | Указывает операции, разрешенные пользователю для зашифрованного PDF-документа. Значение по умолчанию:DisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
