---
title: Bookmark.FirstColumn
linktitle: FirstColumn
articleTitle: FirstColumn
second_title: Aspose.Words for .NET
description: 探索 FirstColumn 属性。轻松访问表格书签范围中第一列的零基索引，实现高效的数据管理。
type: docs
weight: 30
url: /zh/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

获取与书签关联的表格列范围的第一列从零开始的索引。

```csharp
public int FirstColumn { get; }
```

## 评论

返回**-1**如果此书签不是表列书签。

## 例子

展示如何获取有关表列书签的信息。

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // 如果书签包含表的列，则它为表列书签，并且其 IsColumn 标志设置为 true。
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // 打印书签所括的第一列和最后一列的内容。
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### 也可以看看

* class [Bookmark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
