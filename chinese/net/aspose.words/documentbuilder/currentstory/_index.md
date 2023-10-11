---
title: DocumentBuilder.CurrentStory
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 财产. 获取当前在此选择的故事DocumentBuilder.
type: docs
weight: 70
url: /zh/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

获取当前在此选择的故事[`DocumentBuilder`](../).

```csharp
public Story CurrentStory { get; }
```

### 例子

展示如何使用文档生成器的当前故事。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Story 是一种具有子 Paragraph 节点的节点类型，例如 Body。
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// 故事还可以包含表格。
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
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


