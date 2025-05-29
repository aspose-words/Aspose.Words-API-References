---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Saving.HeaderFooterBookmarksExportMode улучшает экспорт закладок в верхних и нижних колонтитулах для бесперебойного управления документами.
type: docs
weight: 5800
url: /ru/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Указывает, как экспортируются закладки в верхних/нижних колонтитулах.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Закладки в верхних/нижних колонтитулах не экспортируются. |
| First | `1` | Экспортируется только закладка в первом колонтитуле раздела. |
| All | `2` | Закладки во всех верхних/нижних колонтитулах экспортируются. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
