---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words for .NET
description: 探索 DocumentBuilder CurrentStory 属性以有效地访问和管理所选故事，增强您的文档编辑体验。
type: docs
weight: 70
url: /zh/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

获取当前选中的故事[`DocumentBuilder`](../).

```csharp
public Story CurrentStory { get; }
```

## 例子

展示如何使用文档构建器的当前故事。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 故事是一种具有子段落节点的节点，例如正文。
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// 故事也可以包含表格。
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### 也可以看看

* class [Story](../../story/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
