---
title: Class Bookmark
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Bookmark 班级. 代表单个书签
type: docs
weight: 40
url: /zh/net/aspose.words/bookmark/
---
## Bookmark class

代表单个书签。

要了解更多信息，请访问[使用书签](https://docs.aspose.com/words/net/working-with-bookmarks/)文档文章。

```csharp
public class Bookmark
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BookmarkEnd](../../aspose.words/bookmark/bookmarkend/) { get; } | 获取表示书签末尾的节点。 |
| [BookmarkStart](../../aspose.words/bookmark/bookmarkstart/) { get; } | 获取表示书签开头的节点。 |
| [FirstColumn](../../aspose.words/bookmark/firstcolumn/) { get; } | 获取与书签关联的表列范围第一列的从零开始的索引。 |
| [IsColumn](../../aspose.words/bookmark/iscolumn/) { get; } | 返回`真的`如果此书签是表列书签. |
| [LastColumn](../../aspose.words/bookmark/lastcolumn/) { get; } | 获取与书签关联的表列范围的最后一列的从零开始的索引。 |
| [Name](../../aspose.words/bookmark/name/) { get; set; } | 获取或设置书签的名称。 |
| [Text](../../aspose.words/bookmark/text/) { get; set; } | 获取或设置书签中包含的文本。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words/bookmark/remove/)() | 从文档中删除书签。不删除书签内的文本。 |

### 评论

`Bookmark`是一个封装了两个节点的“facade”对象[`BookmarkStart`](./bookmarkstart/) 和[`BookmarkEnd`](./bookmarkend/)在文档树中，并允许将书签作为单个对象使用。

### 例子

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

    // 再次打印所有书签以查看更新后的值。
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


