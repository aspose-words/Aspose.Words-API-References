---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder EndColumnBookmark 方法. 将文档中的当前位置标记为列书签末尾该位置必须位于表格单元格中 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

将文档中的当前位置标记为列书签末尾。该位置必须位于表格单元格中。

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 书签的名称。 |

### 返回值

刚刚创建的书签结束节点。

## 评论

列书签覆盖一系列行中的一列或多列。要创建有效的书签，you 需要调用两者[`StartColumnBookmark`](../startcolumnbookmark/)和`EndColumnBookmark`与 same *bookmarkName*范围。

保存文档时，格式错误的书签或名称重复的书签将被忽略。

实际插入的位置[`BookmarkEnd`](../../bookmarkend/)节点可能与当前 document builder 位置不同。

## 例子

展示如何创建列书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// 单元格 1,2,4,5 将被添加书签。
builder.StartColumnBookmark("MyBookmark_1");
// 保存文档时，格式错误的书签或名称重复的书签将被忽略。
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### 也可以看看

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
