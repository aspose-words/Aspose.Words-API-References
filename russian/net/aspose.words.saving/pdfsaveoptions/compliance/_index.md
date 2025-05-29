---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words для .NET
description: Откройте для себя свойство соответствия PdfSaveOptions, чтобы гарантировать, что ваши PDF-документы соответствуют отраслевым стандартам качества и совместимости.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Указывает уровень соответствия стандартам PDF для выходных документов.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Примечания

По умолчаниюPdf17.

## Примеры

Показывает, как установить уровень соответствия стандартам PDF для сохраненных PDF-документов.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
// Обратите внимание, что некоторые параметры PdfSaveOptions запрещены при сохранении в один из стандартов и автоматически исправляются.
// Используйте IWarningCallback, чтобы узнать, какие параметры автоматически исправляются.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите свойство "Compliance" на "PdfCompliance.PdfA1b" для соответствия стандарту "PDF/A-1b",
// который направлен на сохранение визуального вида документа, поскольку Aspose.Words преобразует его в PDF.
// Установите свойство «Compliance» на «PdfCompliance.Pdf17» для соответствия стандарту «1.7».
// Установите свойство "Compliance" на "PdfCompliance.PdfA1a" для соответствия стандарту "PDF/A-1a",
// который соответствует "PDF/A-1b", а также сохраняет структуру исходного документа.
// Установите свойство «Соответствие» на «PdfCompliance.PdfUa1» для соответствия стандарту «PDF/UA-1» (ISO 14289-1),
// целью которого является определение представления электронных документов в формате PDF, позволяющих сделать файл доступным.
// Установите свойство «Соответствие» на «PdfCompliance.Pdf20» для соответствия стандарту «PDF 2.0» (ISO 32000-2).
// Установите свойство «Compliance» на «PdfCompliance.PdfA4» для соответствия стандарту «PDF/A-4» (ISO 19004:2020),
// что сохраняет статический внешний вид документа с течением времени.
// Установите свойство «Соответствие» на «PdfCompliance.PdfA4Ua2» для соответствия PDF/A-4 (ISO 19005-4:2020)
// и стандарты PDF/UA-2 (ISO 14289-2:2024).
// Установите свойство «Соответствие» на «PdfCompliance.PdfUa2» для соответствия стандарту PDF/UA-2 (ISO 14289-2:2024).
// Это помогает сделать документы доступными для поиска, но может значительно увеличить размер и без того больших документов.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Смотрите также

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
