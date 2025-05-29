---
title: DocumentVisitor.VisitBookmarkEnd
linktitle: VisitBookmarkEnd
articleTitle: VisitBookmarkEnd
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentVisitor VisitBookmarkEnd، التي تعمل على تحسين التنقل في المستندات من خلال التعامل بكفاءة مع نهايات الإشارات المرجعية لتوفير تجربة مستخدم سلسة.
type: docs
weight: 40
url: /ar/net/aspose.words/documentvisitor/visitbookmarkend/
---
## DocumentVisitor.VisitBookmarkEnd method

يتم استدعاؤها عند مواجهة نهاية إشارة مرجعية في المستند.

```csharp
public virtual VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkEnd | BookmarkEnd | الشيء الذي يتم زيارته. |

### قيمة الإرجاع

أ[`VisitorAction`](../../visitoraction/) القيمة التي تحدد كيفية مواصلة التعداد.

## أمثلة

يوضح كيفية إضافة الإشارات المرجعية وتحديث محتوياتها.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // قم بإنشاء مستند يحتوي على ثلاثة إشارات مرجعية، ثم استخدم تنفيذ زائر مستند مخصص لطباعة محتوياتها.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    //يمكن الوصول إلى الإشارات المرجعية في مجموعة الإشارات المرجعية عن طريق الفهرس أو الاسم، ويمكن تحديث أسمائها.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // اطبع جميع الإشارات المرجعية مرة أخرى لرؤية القيم المحدثة.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// إنشاء مستند يحتوي على عدد معين من الإشارات المرجعية.
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
/// استخدم متكررًا وزائرًا لطباعة معلومات كل إشارة مرجعية في المجموعة.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    //اجعل كل إشارة مرجعية في المجموعة تقبل زائرًا سيقوم بطباعة محتوياتها.
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
/// طباعة محتويات كل إشارة مرجعية تمت زيارتها على وحدة التحكم.
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

* enum [VisitorAction](../../visitoraction/)
* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentVisitor](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
