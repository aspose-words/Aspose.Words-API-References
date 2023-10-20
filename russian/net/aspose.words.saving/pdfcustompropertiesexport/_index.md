---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.PdfCustomPropertiesExport перечисление. Указывает путьCustomDocumentProperties экспортируются в файл PDF на С#.
type: docs
weight: 5420
url: /ru/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Указывает путь[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) экспортируются в файл PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Никакие пользовательские свойства не экспортируются. |
| Standard | `1` | Пользовательские свойства экспортируются как записи в словаре /Info. |
| Metadata | `2` | Пользовательские свойства — это метаданные. |

## Примеры

Показывает, как экспортировать пользовательские свойства при преобразовании документа в PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «CustomPropertiesExport» значение «PdfCustomPropertiesExport.None», чтобы отбросить
// пользовательские свойства документа при сохранении документа в формате .PDF.
// Установите для свойства «CustomPropertiesExport» значение «PdfCustomPropertiesExport.Standard»
// чтобы сохранить пользовательские свойства в выходном PDF-документе.
// Установите для свойства «CustomPropertiesExport» значение «PdfCustomPropertiesExport.Metadata»
// чтобы сохранить пользовательские свойства в пакете XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
