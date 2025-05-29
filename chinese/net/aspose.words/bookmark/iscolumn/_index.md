---
title: Bookmark.IsColumn
linktitle: IsColumn
articleTitle: IsColumn
second_title: Aspose.Words for .NET
description: 探索 IsColumn 属性。轻松识别书签是否代表表格列，增强文档导航和组织功能。
type: docs
weight: 40
url: /zh/net/aspose.words/bookmark/iscolumn/
---
## Bookmark.IsColumn property

返回`真的`如果此书签是表列书签。

```csharp
public bool IsColumn { get; }
```

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
