---
title: Class BookmarkCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.BookmarkCollection فصل. مجموعة منBookmark الكائنات التي تمثل الإشارات المرجعية في النطاق المحدد.
type: docs
weight: 50
url: /ar/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

مجموعة من[`Bookmark`](../bookmark/) الكائنات التي تمثل الإشارات المرجعية في النطاق المحدد.

لمعرفة المزيد، قم بزيارة[العمل مع الإشارات المرجعية](https://docs.aspose.com/words/net/working-with-bookmarks/) مقالة توثيقية.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | إرجاع عدد الإشارات المرجعية في المجموعة. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | إرجاع إشارة مرجعية في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | إزالة كافة الإشارات المرجعية من هذه المجموعة ومن المستند. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | يُرجع كائن العداد. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(Bookmark) | إزالة الإشارة المرجعية المحددة من المستند. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(string) | إزالة إشارة مرجعية بالاسم المحدد. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(int) | إزالة الإشارة المرجعية في الفهرس المحدد. |

### أمثلة

يوضح كيفية إضافة الإشارات المرجعية وتحديث محتوياتها.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // أنشئ مستندًا يحتوي على ثلاث إشارات مرجعية، ثم استخدم تطبيق زائر المستند المخصص لطباعة محتوياتها.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // يمكن الوصول إلى الإشارات المرجعية في مجموعة الإشارات المرجعية عن طريق الفهرس أو الاسم، ويمكن تحديث أسمائها.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // اطبع جميع الإشارات المرجعية مرة أخرى لرؤية القيم المحدثة.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// أنشئ مستندًا يحتوي على عدد معين من الإشارات المرجعية.
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
/// استخدم المكرر والزائر لطباعة معلومات كل إشارة مرجعية في المجموعة.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // احصل على كل إشارة مرجعية في المجموعة لقبول الزائر الذي سيطبع محتوياتها.
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
/// يطبع محتويات كل إشارة مرجعية تمت زيارتها إلى وحدة التحكم.
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

### أنظر أيضا

* class [Bookmark](../bookmark/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


