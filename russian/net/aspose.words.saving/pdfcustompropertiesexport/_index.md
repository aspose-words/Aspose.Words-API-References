---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words.PdfCustomPropertiesExport улучшает экспорт PDF-файлов за счет настройки свойств документа для достижения оптимальных результатов.
type: docs
weight: 6210
url: /ru/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Указывает способ[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) экспортируются в файл PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Пользовательские свойства не экспортируются. |
| Standard | `1` | Пользовательские свойства экспортируются как записи в /Info dictionary. |
| Metadata | `2` | Пользовательские свойства — это метаданные. |

## Примеры

Показывает, как экспортировать пользовательские свойства при конвертации документа в PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "CustomPropertiesExport" на "PdfCustomPropertiesExport.None", чтобы отменить
// пользовательские свойства документа при сохранении документа в формате .PDF.
// Установите свойство "CustomPropertiesExport" на "PdfCustomPropertiesExport.Standard"
// для сохранения пользовательских свойств в выходном PDF-документе.
// Установите свойство "CustomPropertiesExport" на "PdfCustomPropertiesExport.Metadata"
// для сохранения пользовательских свойств в пакете XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
