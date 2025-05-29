---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.BookmarkCollection — мощный инструмент для управления закладками в документах, улучшения организации и навигации.
type: docs
weight: 240
url: /ru/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Коллекция[`Bookmark`](../bookmark/) объекты, представляющие закладки в указанном диапазоне.

Чтобы узнать больше, посетите[Работа с закладками](https://docs.aspose.com/words/net/working-with-bookmarks/) документальная статья.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Возвращает количество закладок в коллекции. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Возвращает закладку по указанному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Удаляет все закладки из этой коллекции и из документа. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | Удаляет указанную закладку из документа. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | Удаляет закладку с указанным именем. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | Удаляет закладку по указанному индексу. |

## Примеры

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Создайте документ с тремя закладками, затем используйте пользовательскую реализацию посетителя документа для печати их содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Доступ к закладкам в коллекции закладок можно осуществлять по индексу или имени, а их имена можно обновлять.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Распечатайте все закладки еще раз, чтобы увидеть обновленные значения.
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
/// Используйте итератор и посетителя для вывода информации о каждой закладке в коллекции.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Заставить каждую закладку в коллекции принять посетителя, который распечатает ее содержимое.
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

* class [Bookmark](../bookmark/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
