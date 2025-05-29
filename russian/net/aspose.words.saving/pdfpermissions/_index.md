---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PdfPermissions для управления доступом пользователей к зашифрованным PDF-файлам. Повысьте безопасность и эффективно управляйте операциями с документами.
type: docs
weight: 6310
url: /ru/net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Указывает операции, разрешенные пользователю для зашифрованного PDF-документа.

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
| ContentCopyForAccessibility | `200` | Извлечение текста и графики (в поддержку доступности для пользователей с ограниченными возможностями или для других целей). |
| ModifyContents | `8` | Изменить содержимое документа с помощью операций, отличных от тех, которые контролируются ModifyAnnotations ,FillIn , иDocumentAssembly . |
| ModifyAnnotations | `20` | Добавьте или измените текстовые аннотации, заполните поля интерактивной формы и, еслиModifyContents is также устанавливает, создает или изменяет поля интерактивной формы (включая поля подписи). |
| FillIn | `100` | Заполните существующие поля интерактивной формы (включая поля подписи), даже еслиModifyContents ясно. |
| DocumentAssembly | `400` | Соберите документ (вставьте, поверните или удалите страницы и создайте элементы структуры документа или миниатюры изображений), даже еслиModifyContents ясно. |
| Printing | `4` | Распечатать документ (возможно, не на самом высоком уровне качества, в зависимости от того, HighResolutionPrinting также установлено). |
| HighResolutionPrinting | `804` | Печать документа в виде, из которого может быть сгенерирована точная цифровая копия содержимого PDF на основе алгоритма, зависящего от реализации. Когда этот флаг сброшен (and Printing установлено), печать должна быть ограничена низкоуровневым представлением внешнего вида, возможно ухудшенного качества. |

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
