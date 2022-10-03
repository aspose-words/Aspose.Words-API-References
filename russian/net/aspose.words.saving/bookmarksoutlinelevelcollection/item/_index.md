---
title: Item
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает уровень структуры закладки по имени закладки.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Получает или задает уровень структуры закладки по имени закладки.

```csharp
public int this[string name] { get; set; }
```

| Параметр | Описание |
| --- | --- |
| name | Нечувствительное к регистру имя закладки. |

### Возвращаемое значение

Уровень контура закладки. Допустимый диапазон от 0 до 9.

### Примеры

Показывает, как установить уровни структуры для закладок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить закладку с другой закладкой, вложенной в нее.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Вставить другую закладку.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// При сохранении в формате .pdf доступ к закладкам можно получить через раскрывающееся меню, и большинство читателей могут использовать их в качестве привязок.
// Закладки также могут иметь числовые значения для уровней структуры,
// позволяет элементам структуры более низкого уровня скрывать дочерние элементы более высокого уровня при сворачивании в считывателе.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Мы можем удалить два элемента, чтобы осталось только обозначение уровня контура для «Закладки 1».
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Имеется девять уровней структуры. Их нумерация будет оптимизирована во время операции сохранения.
// В этом случае уровни "5" и "9" станут "2" и "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Очистка этой коллекции сохранит закладки и поместит их все на один и тот же уровень структуры.
outlineLevels.Clear();
```

### Смотрите также

* class [BookmarksOutlineLevelCollection](../)
* пространство имен [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* сборка [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Получает или задает уровень структуры закладки по указанному индексу.

```csharp
public int this[int index] { get; set; }
```

| Параметр | Описание |
| --- | --- |
| index | Отсчитываемый от нуля индекс закладки. |

### Возвращаемое значение

Уровень контура закладки. Допустимый диапазон от 0 до 9.

### Примеры

Показывает, как установить уровни структуры для закладок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить закладку с другой закладкой, вложенной в нее.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Вставить другую закладку.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// При сохранении в формате .pdf доступ к закладкам можно получить через раскрывающееся меню, и большинство читателей могут использовать их в качестве привязок.
// Закладки также могут иметь числовые значения для уровней структуры,
// позволяет элементам структуры более низкого уровня скрывать дочерние элементы более высокого уровня при сворачивании в считывателе.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Мы можем удалить два элемента, чтобы осталось только обозначение уровня контура для «Закладки 1».
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Имеется девять уровней структуры. Их нумерация будет оптимизирована во время операции сохранения.
// В этом случае уровни "5" и "9" станут "2" и "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Очистка этой коллекции сохранит закладки и поместит их все на один и тот же уровень структуры.
outlineLevels.Clear();
```

### Смотрите также

* class [BookmarksOutlineLevelCollection](../)
* пространство имен [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
