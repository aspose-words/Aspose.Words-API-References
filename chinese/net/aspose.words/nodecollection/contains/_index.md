---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words for .NET
description: 了解 NodeCollection Contains 方法如何有效地检查集合中是否存在节点，从而增强数据管理能力。
type: docs
weight: 50
url: /zh/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

确定节点是否在集合中。

```csharp
public bool Contains(Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node | Node | 要定位的节点。 |

### 返回值

`真的`如果在集合中找到该项目；否则，`错误的`。

## 评论

该方法执行线性搜索；因此，平均执行时间与[`Count`](../count/)。

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
