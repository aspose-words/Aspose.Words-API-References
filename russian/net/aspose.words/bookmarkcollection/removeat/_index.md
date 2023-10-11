---
title: BookmarkCollection.RemoveAt
second_title: Справочник по API Aspose.Words для .NET
description: BookmarkCollection метод. Удаляет закладку по указанному индексу.
type: docs
weight: 60
url: /ru/net/aspose.words/bookmarkcollection/removeat/
---
## BookmarkCollection.RemoveAt method

Удаляет закладку по указанному индексу.

```csharp
public void RemoveAt(int index)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Отсчитываемый от нуля индекс закладки, которую нужно удалить. |

### Примеры

Показывает, как удалить закладки из документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем пять закладок с текстом внутри их границ.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Эта коллекция хранит закладки.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Существует несколько способов удаления закладок.
// 1 - Вызов метода Remove закладки:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 – Передача закладки в метод Remove коллекции:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

//3 - Удаление закладки из коллекции по имени:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Удаление закладки по индексу в коллекции закладок:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Мы можем очистить всю коллекцию закладок.
bookmarks.Clear();

// Текст, который был внутри закладок, все еще присутствует в документе.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Смотрите также

* class [BookmarkCollection](../)
* пространство имен [Aspose.Words](../../bookmarkcollection/)
* сборка [Aspose.Words](../../../)


