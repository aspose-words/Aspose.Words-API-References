---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用 NodeCollection Remove 方法轻松地从文档中删除节点，从而简化数据管理并提高性能。
type: docs
weight: 90
url: /zh/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

从集合和文档中删除节点。

```csharp
public void Remove(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 要移除的节点。 |

## 例子

展示如何使用 NodeCollection。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 通过使用 DocumentBuilder 插入 Runs 向文档添加文本。
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// 每次调用“Write”方法都会创建一个新的 Run，
// 然后出现在父 Paragraph 的 RunCollection 中。
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// 我们也可以手动将节点插入到 RunCollection 中。
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// 访问单个运行并将其删除以从文档中删除其文本。
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### 也可以看看

* class [Node](../../node/)
* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
