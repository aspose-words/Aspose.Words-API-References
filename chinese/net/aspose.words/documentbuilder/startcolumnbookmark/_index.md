---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 StartColumnBookmark 方法可以轻松地将表格单元格位置标记为列书签，从而增强文档导航和组织。
type: docs
weight: 660
url: /zh/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

将文档中的当前位置标记为列书签的起始位置。该位置必须位于表格单元格中。

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 书签的名称。 |

### 返回值

刚刚创建的书签起始节点。

## 评论

列书签涵盖行范围内的一列或多列。要创建有效的书签，您需要同时调用`StartColumnBookmark`和[`EndColumnBookmark`](../endcolumnbookmark/)具有相同 *bookmarkName*范围。

保存文档时，格式不正确的书签或名称重复的书签将被忽略。

插入的实际位置[`BookmarkStart`](../../bookmarkstart/)节点可能与当前 document 构建器位置不同。

## 例子

展示如何创建列书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// 单元格 1、2、4、5 将被添加书签。
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

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
