---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Справочник по API Aspose.Words для .NET
description: OutlineOptions свойство. Указывает уровень по умолчанию в структуре документа на котором отображаются закладки Word.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Указывает уровень по умолчанию в структуре документа, на котором отображаются закладки Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### Примечания

Уровень отдельных закладок можно указать с помощью[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) свойство.

Укажите 0, и закладки Word не будут отображаться в структуре документа. Укажите 1, и закладки Word будут отображаться в структуре документа на уровне 1; 2 для уровня 2 и так далее.

По умолчанию — 0. Допустимый диапазон — от 0 до 9.

### Примеры

Показывает обработку закладок в верхних и нижних колонтитулах документа, который мы преобразуем в PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства «PageMode» значение «PdfPageMode.UseOutlines», чтобы отобразить контурную панель навигации в выходном PDF-файле.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Установите для свойства «DefaultBookmarksOutlineLevel» значение «1», чтобы отобразить все
// закладки на первом уровне структуры в выходном PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Установите для свойства «HeaderFooterBookmarksExportMode» значение «HeaderFooterBookmarksExportMode.None», чтобы
// не экспортировать закладки, находящиеся внутри верхних/нижних колонтитулов.
// Установите для свойства "HeaderFooterBookmarksExportMode" значение "HeaderFooterBookmarksExportMode.First", чтобы
// экспортируем только закладки в верхнем/нижнем колонтитуле первого раздела.
// Установите для свойства «HeaderFooterBookmarksExportMode» значение «HeaderFooterBookmarksExportMode.All», чтобы
// экспортируем закладки, которые есть во всех верхних/нижних колонтитулах.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../outlineoptions/)
* сборка [Aspose.Words](../../../)


