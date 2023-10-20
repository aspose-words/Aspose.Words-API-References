---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.PdfPermissions перечисление. Указывает операции которые разрешены пользователю с зашифрованным PDFдокументом на С#.
type: docs
weight: 5510
url: /ru/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Указывает операции, которые разрешены пользователю с зашифрованным PDF-документом.

```csharp
[Flags]
public enum PdfPermissions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| DisallowAll | `0` | Запрещает все операции с PDF-документом. Это значение по умолчанию. |
| AllowAll | `FFFF` | Разрешает все операции с PDF-документом. |
| ContentCopy | `10` | Копировать или иным образом извлекать текст и графику из документа с помощью операций, отличных от контролируемых ContentCopyForAccessibility . |
| ContentCopyForAccessibility | `200` | Извлечение текста и графики (для обеспечения доступности для пользователей с ограниченными возможностями или для других целей). |
| ModifyContents | `8` | Изменить содержимое документа с помощью операций, отличных от тех, которые контролируются ModifyAnnotations ,FillIn , иDocumentAssembly . |
| ModifyAnnotations | `20` | Добавляйте или изменяйте текстовые аннотации, заполняйте поля интерактивной формы и, еслиModifyContents is также устанавливает, создает или изменяет поля интерактивной формы (включая поля подписи). |
| FillIn | `100` | Заполните существующие поля интерактивной формы (включая поля для подписи), даже еслиModifyContents ясно. |
| DocumentAssembly | `400` | Соберите документ (вставьте, поверните или удалите страницы и создайте элементы структуры документа или миниатюры изображений), даже еслиModifyContents ясно. |
| Printing | `4` | Распечатайте документ (возможно, не с самым высоким уровнем качества, в зависимости от того, будет ли HighResolutionPrinting также установлен). |
| HighResolutionPrinting | `804` | Распечатайте документ в представлении, из которого может быть создана точная цифровая копия содержимого PDF-файла на основе алгоритма, зависящего от реализации. Когда этот флаг сброшен (and Printing установлен), печать должна быть ограничена низкоуровневым представлением внешнего вида, , возможно, с ухудшенным качеством. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
