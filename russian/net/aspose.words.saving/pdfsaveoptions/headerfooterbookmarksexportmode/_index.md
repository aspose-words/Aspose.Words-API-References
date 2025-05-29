---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PdfSaveOptions HeaderFooterBookmarksExportMode оптимизирует экспорт закладок в верхних и нижних колонтитулах для улучшения функциональности PDF.
type: docs
weight: 180
url: /ru/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

Определяет, как экспортируются закладки в верхних/нижних колонтитулах.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## Примечания

Значение по умолчанию:All.

Это свойство используется совместно с[`OutlineOptions`](../outlineoptions/) вариант.

## Примеры

Показывает, как обрабатывать закладки в верхних/нижних колонтитулах документа, который мы преобразуем в PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите свойство «PageMode» на «PdfPageMode.UseOutlines», чтобы отобразить панель навигации структуры в выходном PDF-файле.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Установите свойство "DefaultBookmarksOutlineLevel" на "1", чтобы отобразить все
// закладки на первом уровне структуры в выходном PDF-файле.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.None" для
// не экспортировать закладки, находящиеся внутри верхних/нижних колонтитулов.
// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.First" для
// экспортировать закладки только в верхних/нижних колонтитулах первого раздела.
// Установите свойство "HeaderFooterBookmarksExportMode" в значение "HeaderFooterBookmarksExportMode.All" для
// экспортировать закладки, находящиеся во всех верхних/нижних колонтитулах.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Смотрите также

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
