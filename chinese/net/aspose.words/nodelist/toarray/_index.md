---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: 用于 .NET 的 Aspose.Words
description: NodeList ToArray 方法. 将集合中的所有节点复制到新的节点数组 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

将集合中的所有节点复制到新的节点数组。

```csharp
public Node[] ToArray()
```

### 返回值

节点数组。

## 评论

您不应在迭代节点集合 时添加/删除节点，因为这会使迭代器无效并且需要刷新实时集合。

为了能够在迭代期间添加/删除节点，请使用此方法将 节点复制到固定大小的数组中，然后迭代该数组。

## 例子

演示如何使用 XPath 表达式选择某些节点。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 该表达式将提取所有段落节点，
// 它们是文档中任何表节点的后代。
NodeList nodeList = doc.SelectNodes("//表格//段落");

// 使用枚举器遍历列表并打印表的每个单元格中每个段落的内容。
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// 此表达式将选择文档中任何 Body 节点的直接子级的任何段落。
nodeList = doc.SelectNodes("//正文/段落");

// 我们可以将列表视为数组。
Assert.AreEqual(4, nodeList.ToArray().Length);

// 使用 SelectSingleNode 选择与上面相同的表达式的第一个结果。
Node node = doc.SelectSingleNode("//正文/段落");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### 也可以看看

* class [Node](../../node/)
* class [NodeList](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
