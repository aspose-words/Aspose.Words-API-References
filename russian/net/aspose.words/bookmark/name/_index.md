---
title: Bookmark.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Bookmark Name свойство. Получает или задает имя закладки на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

Получает или задает имя закладки.

```csharp
public string Name { get; set; }
```

## Примечания

Обратите внимание: если вы измените имя закладки на имя, которое уже существует в документе, ошибка не возникнет, и при сохранении документа будет сохранена только первая закладка.

## Примеры

Показывает, как вставить закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);            

// Действительная закладка имеет имя, узел BookmarkStart и BookmarkEnd.
// Любые пробелы в именах закладок будут преобразованы в символы подчеркивания, если мы откроем сохраненный документ в Microsoft Word.
// Если мы выделим имя закладки в Microsoft Word с помощью Insert -> gt; Ссылки -> Добавьте в закладки и нажмите «Перейти»,
// курсор перейдет к тексту, заключенному между узлами BookmarkStart и BookmarkEnd.
builder.StartBookmark("My Bookmark");
builder.Write("Contents of MyBookmark.");
builder.EndBookmark("My Bookmark");

// Закладки хранятся в этой коллекции.
Assert.AreEqual("My Bookmark", doc.Range.Bookmarks[0].Name);

doc.Save(ArtifactsDir + "Bookmarks.Insert.docx");
```

Показывает, как добавлять закладки и обновлять их содержимое.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Создайте документ с тремя закладками, затем используйте специальную реализацию посетителя документа для печати его содержимого.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // Доступ к закладкам в коллекции закладок можно получить по индексу или имени, а их имена можно обновить.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Распечатываем все закладки еще раз, чтобы увидеть обновленные значения.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Создаем документ с заданным количеством закладок.
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
/// Выводит на консоль содержимое каждой посещенной закладки.
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

* class [Bookmark](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
