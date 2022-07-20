---
title: BookmarkEnd
second_title: Aspose.Words لمراجع .NET API
description: يمثل نهاية إشارة مرجعية في مستند Word.
type: docs
weight: 50
url: /ar/net/aspose.words/bookmarkend/
---
## BookmarkEnd class

يمثل نهاية إشارة مرجعية في مستند Word.

```csharp
public class BookmarkEnd : Node
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [BookmarkEnd](bookmarkend)(DocumentBase, string) | يقوم بتهيئة مثيل جديد لملف[`BookmarkEnd`](../bookmarkend) فئة ._ x000d_ |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | يحدد معرف العقدة المخصص ._ x000d_ |
| virtual [Document](../../aspose.words/node/document) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [Name](../../aspose.words/bookmarkend/name) { get; set; } | الحصول على اسم الإشارة المرجعية أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/bookmarkend/nodetype) { get; } | عوائدBookmarkEnd . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/bookmarkend/accept)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext)() | يحصل على نص هذه العقدة وجميع توابعها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

تتكون الإشارة المرجعية الكاملة في مستند Word من ملف[`BookmarkStart`](../bookmarkstart) ومطابقة[`BookmarkEnd`](../bookmarkend) بنفس اسم الإشارة المرجعية.

[`BookmarkStart`](../bookmarkstart) و[`BookmarkEnd`](../bookmarkend) هي مجرد علامات داخل document تحدد مكان بدء الإشارة المرجعية ونهايتها.

استخدم ال[`Bookmark`](../bookmark) فئة كـ "واجهة" للعمل مع bookmark ككائن واحد.

### أمثلة

يوضح كيفية إضافة الإشارات المرجعية وتحديث محتوياتها.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // أنشئ مستندًا بثلاث إشارات مرجعية ، ثم استخدم تنفيذ زائر مستند مخصص لطباعة محتوياتها.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // يمكن الوصول إلى الإشارات المرجعية في مجموعة الإشارات المرجعية بالفهرس أو الاسم ، ويمكن تحديث أسمائها.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // طباعة جميع الإشارات المرجعية مرة أخرى لرؤية القيم المحدثة.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// أنشئ مستندًا بعدد معين من الإشارات المرجعية.
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
/// استخدم مكررًا وزائرًا لطباعة معلومات كل إشارة مرجعية في المجموعة.
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
/// يطبع محتويات كل إشارة مرجعية تمت زيارتها على وحدة التحكم.
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

* class [Node](../node)
* مساحة الاسم [Aspose.Words](../../aspose.words)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
