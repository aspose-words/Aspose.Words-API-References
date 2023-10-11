---
title: Enum HeaderFooterBookmarksExportMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode перечисление. Указывает как экспортируются закладки в верхних и нижних колонтитулах.
type: docs
weight: 5050
url: /ru/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Указывает, как экспортируются закладки в верхних и нижних колонтитулах.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Закладки в верхних/нижних колонтитулах не экспортируются. |
| First | `1` | Экспортируется только закладка в первом колонтитуле раздела. |
| All | `2` | Закладки во всех верхних и нижних колонтитулах экспортируются. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


