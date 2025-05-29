---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PdfSaveOptions CustomPropertiesExport улучшает экспорт PDF-файлов, управляя CustomDocumentProperties для достижения оптимальных результатов.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Возвращает или задает значение, определяющее способ[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) экспортируются в файл PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Примечания

Значение по умолчанию:None.

Metadata значение не поддерживается при сохранении в PDF/A. Standard будет использоваться вместо PDF/A-1 и PDF/A-2 and None для PDF/A-4.

Standard значение не поддерживается при сохранении в PDF 2.0. Metadata Вместо этого будет использоваться .

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
