---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или устанавливает значение определяющее способCustomDocumentProperties экспортируются в файл PDF.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Получает или устанавливает значение, определяющее способ[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) экспортируются в файл PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### Примечания

Значение по умолчанию:None.

Metadata значение не поддерживается при сохранении в PDF/A. Standard вместо этого будет использоваться для PDF/A-1 и PDF/A-2 and None для PDF/A-4.

Standard значение не поддерживается при сохранении в PDF 2.0. Metadata вместо этого будет использоваться.

### Примеры

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


