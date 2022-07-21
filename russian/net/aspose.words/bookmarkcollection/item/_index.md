---
title: Item
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает закладку по указанному индексу.
type: docs
weight: 20
url: /ru/net/aspose.words/bookmarkcollection/item/
---
## BookmarkCollection indexer (1 of 2)

Возвращает закладку по указанному индексу.

```csharp
public Bookmark this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в коллекции. |

### Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

### Примеры

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Создайте документ с тремя закладками, затем используйте пользовательскую реализацию посетителя документа для печати их содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Доступ к закладкам в коллекции закладок можно получить по индексу или имени, и их имена можно обновить.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Печатаем все закладки еще раз, чтобы увидеть обновленные значения.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Создать документ с заданным количеством закладок.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Используйте итератор и посетитель для вывода информации о каждой закладке в коллекции.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Получить каждую закладку в коллекции, чтобы принять посетителя, который распечатает ее содержимое.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Выводит содержимое каждой посещенной закладки на консоль.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Смотрите также

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* пространство имен [Aspose.Words](../../bookmarkcollection)
* сборка [Aspose.Words](../../../)

---

## BookmarkCollection indexer (2 of 2)

Возвращает закладку по имени.

```csharp
public Bookmark this[string bookmarkName] { get; }
```

| Параметр | Описание |
| --- | --- |
| bookmarkName | Нечувствительное к регистру имя закладки. |

### Примечания

Возвращает null, если закладка с указанным именем не может быть найдена.

### Примеры

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Создайте документ с тремя закладками, затем используйте пользовательскую реализацию посетителя документа для печати их содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Доступ к закладкам в коллекции закладок можно получить по индексу или имени, и их имена можно обновить.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Печатаем все закладки еще раз, чтобы увидеть обновленные значения.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Создать документ с заданным количеством закладок.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Используйте итератор и посетитель для вывода информации о каждой закладке в коллекции.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Получить каждую закладку в коллекции, чтобы принять посетителя, который распечатает ее содержимое.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Выводит содержимое каждой посещенной закладки на консоль.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Смотрите также

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* пространство имен [Aspose.Words](../../bookmarkcollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
