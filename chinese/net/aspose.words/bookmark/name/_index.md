---
title: Bookmark.Name
second_title: Aspose.Words for .NET API 参考
description: Bookmark 财产. 获取或设置书签的名称
type: docs
weight: 60
url: /zh/net/aspose.words/bookmark/name/
---
## Bookmark.Name property

获取或设置书签的名称。

```csharp
public string Name { get; set; }
```

### 评论

请注意，如果您将书签的名称更改为文档中已存在的名称， 不会出现错误，并且在您保存文档时只会存储第一个书签。

### 例子

显示如何插入书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 一个有效的书签有一个名字、一个 BookmarkStart 和一个 BookmarkEnd 节点。
// 如果我们用 Microsoft Word 打开保存的文档，书签名称中的任何空格都将转换为下划线。 
// 如果我们通过插入在 Microsoft Word 中突出显示书签的名称 ->链接->加入书签，然后按“转到”，
// 光标将跳转到 BookmarkStart 和 BookmarkEnd 节点之间的文本。
builder.StartBookmark("My Bookmark");
builder.Write("Contents of MyBookmark.");
builder.EndBookmark("My Bookmark");

// 书签存储在此集合中。
Assert.AreEqual("My Bookmark", doc.Range.Bookmarks[0].Name);

doc.Save(ArtifactsDir + "Bookmarks.Insert.docx");
```

展示如何添加书签和更新其内容。

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // 创建一个包含三个书签的文档，然后使用自定义文档访问者实现来打印其内容。
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // 书签集合中可以通过索引或名称访问书签，并且可以更新它们的名称。
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // 再次打印所有书签以查看更新的值。
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// 创建一个具有给定数量书签的文档。
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

* class [Bookmark](../)
* 命名空间 [Aspose.Words](../../bookmark/)
* 部件 [Aspose.Words](../../../)


