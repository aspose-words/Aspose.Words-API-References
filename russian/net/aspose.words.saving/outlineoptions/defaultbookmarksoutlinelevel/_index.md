---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words для .NET
description: Узнайте, как свойство DefaultBookmarksOutlineLevel улучшает ваши документы Word, оптимизируя видимость закладок в структуре. Повысьте производительность сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Указывает уровень по умолчанию в структуре документа, на котором следует отображать закладки Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Примечания

Индивидуальный уровень закладок можно указать с помощью[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) свойство.

Укажите 0, и закладки Word не будут отображаться в структуре документа. Укажите 1, и закладки Word будут отображаться в структуре документа на уровне 1; 2 для уровня 2 и т. д.

По умолчанию — 0. Допустимый диапазон — от 0 до 9.

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

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
