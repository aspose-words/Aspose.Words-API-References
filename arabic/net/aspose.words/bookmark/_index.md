---
title: Class Bookmark
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Bookmark فصل. يمثل إشارة مرجعية واحدة.
type: docs
weight: 40
url: /ar/net/aspose.words/bookmark/
---
## Bookmark class

يمثل إشارة مرجعية واحدة.

لمعرفة المزيد، قم بزيارة[العمل مع الإشارات المرجعية](https://docs.aspose.com/words/net/working-with-bookmarks/) مقالة توثيقية.

```csharp
public class Bookmark
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | يحصل على العقدة التي تمثل نهاية الإشارة المرجعية. |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | يحصل على العقدة التي تمثل بداية الإشارة المرجعية. |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | الحصول على الفهرس الصفري للعمود الأول من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | إرجاع`حقيقي` إذا كانت هذه الإشارة المرجعية عبارة عن إشارة مرجعية لعمود الجدول. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | الحصول على الفهرس الصفري للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | الحصول على اسم الإشارة المرجعية أو تعيينه. |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | الحصول على النص الموجود في الإشارة المرجعية أو تعيينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | إزالة الإشارة المرجعية من المستند. لا يزيل النص الموجود داخل الإشارة المرجعية. |

### ملاحظات

`Bookmark` هو كائن "واجهة" يحتوي على عقدتين[`BookmarkStart`](./bookmarkstart/) و[`BookmarkEnd`](./bookmarkend/) في شجرة المستندات ويسمح بالعمل مع الإشارة المرجعية ككائن واحد.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


