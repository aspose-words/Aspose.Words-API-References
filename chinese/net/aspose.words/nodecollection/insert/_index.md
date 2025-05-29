---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words for .NET
description: 使用我们精简的插入方法，轻松将节点插入到 NodeCollection 的任意索引处。立即增强您的数据管理！
type: docs
weight: 80
url: /zh/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

将节点插入到指定索引的集合中。

```csharp
public void Insert(int index, Node node)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 节点的从零开始的索引。 允许使用负索引，表示从列表后面进行访问。 例如，-1 表示最后一个节点，-2 表示倒数第二个节点，依此类推。 |
| node | Node | 要插入的节点。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| NotSupportedException | 这[`NodeCollection`](../)是一个“深度”收藏。 |

## 评论

该节点作为子节点插入到创建集合的节点对象中。

如果索引等于或大于[`Count`](../count/)，该节点被添加到集合的末尾。

如果指数为负数，且其绝对值大于[`Count`](../count/)，该节点被添加到集合的末尾。

如果插入的节点是从另一个文档创建的，则应使用 [`ImportNode`](../../documentbase/importnode/)将节点导入当前文档。 然后可以将导入的节点插入到当前文档中。

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
