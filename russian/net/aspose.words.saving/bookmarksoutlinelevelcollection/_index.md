---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.BookmarksOutlineLevelCollection — мощный инструмент для управления закладками и улучшения навигации по документу без особых усилий.
type: docs
weight: 5590
url: /ru/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Коллекция отдельных закладок уровня структуры.

Чтобы узнать больше, посетите[Работа с закладками](https://docs.aspose.com/words/net/working-with-bookmarks/) документальная статья.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Получает или задает уровень структуры закладки по имени закладки. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Добавляет закладку в коллекцию. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Удаляет все элементы из коллекции. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Определяет, содержит ли коллекция закладку с указанным именем. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов в коллекции. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Возвращает индекс указанной закладки в коллекции (начиная с нуля). |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Удаляет закладку с указанным именем из коллекции. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Удаляет закладку по указанному индексу. |

## Примечания

Ключ — это нечувствительное к регистру строковое имя закладки. Значение — это уровень структуры закладки int.

Уровень структуры закладки может иметь значение от 0 до 9. Укажите 0, и закладка Word не будет отображаться в структуре документа. Укажите 1, и закладка Word будет отображаться в структуре документа на уровне 1; 2 для уровня 2 и т. д.

## Примеры

Показывает, как устанавливать уровни структуры для закладок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить закладку с другой вложенной в нее закладкой.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Вставить еще одну закладку.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// При сохранении в формате .pdf закладки доступны через раскрывающееся меню и используются в качестве якорей большинством читателей.
// Закладки также могут иметь числовые значения для уровней структуры,
// включение записей структуры более низкого уровня для скрытия дочерних записей более высокого уровня при свертывании в программе чтения.
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

// Мы можем удалить два элемента, чтобы осталось только обозначение уровня структуры для «Закладки 1».
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Всего девять уровней структуры. Их нумерация будет оптимизирована во время операции сохранения.
// В этом случае уровни «5» и «9» станут «2» и «3».
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Очистка этой коллекции сохранит закладки и поместит их все на один уровень структуры.
outlineLevels.Clear();
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
