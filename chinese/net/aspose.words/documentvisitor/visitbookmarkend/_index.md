---
title: DocumentVisitor.VisitBookmarkEnd
linktitle: VisitBookmarkEnd
articleTitle: VisitBookmarkEnd
second_title: Aspose.Words for .NET
description: 探索 DocumentVisitor VisitBookmarkEnd 方法，该方法通过有效处理书签结尾来增强文档导航，从而实现无缝的用户体验。
type: docs
weight: 40
url: /zh/net/aspose.words/documentvisitor/visitbookmarkend/
---
## DocumentVisitor.VisitBookmarkEnd method

当文档中遇到书签末尾时调用。

```csharp
public virtual VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkEnd | BookmarkEnd | 正在访问的对象。 |

### 返回值

一个[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 例子

展示如何添加书签并更新其内容。

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // 创建一个包含三个书签的文档，然后使用自定义文档访问者实现来打印其内容。
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // 可以通过索引或名称在书签集合中访问书签，并且可以更新其名称。
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // 再次打印所有书签以查看更新的值。
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// 创建具有给定数量书签的文档。
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
/// 使用迭代器和访问者打印集合中每个书签的信息。
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // 获取集合中的每个书签以接受将打印其内容的访问者。
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
/// 将每个访问过的书签的内容打印到控制台。
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

### 也可以看看

* enum [VisitorAction](../../visitoraction/)
* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
