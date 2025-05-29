---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.OutlineOptions, чтобы настроить параметры структуры документа для лучшей организации и ясности.
type: docs
weight: 6140
url: /ru/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Позволяет указать параметры контура.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class OutlineOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Позволяет указать индивидуальный уровень структуры закладок. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Возвращает или задает значение, определяющее, следует ли создавать отсутствующие уровни структуры при экспорте документа . |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Указывает, следует ли создавать контуры для заголовков (абзацев, отформатированных с использованием стилей заголовков) внутри таблиц. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Указывает уровень по умолчанию в структуре документа, на котором следует отображать закладки Word. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Указывает, сколько уровней в структуре документа будет отображаться развернутым при просмотре файла. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Указывает, сколько уровней заголовков (абзацев, отформатированных с использованием стилей заголовков) следует включить в структуру документа . |

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
