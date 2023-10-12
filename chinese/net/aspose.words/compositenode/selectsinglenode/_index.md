---
title: CompositeNode.SelectSingleNode
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 方法. 选择第一个Node与 XPath 表达式匹配
type: docs
weight: 220
url: /zh/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

选择第一个[`Node`](../../node/)与 XPath 表达式匹配。

```csharp
public Node SelectSingleNode(string xpath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | String | XPath 表达式。 |

### 返回值

首先[`Node`](../../node/)匹配 XPath 查询或`无效的`如果没有找到匹配的节点。

### 评论

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式 。

### 例子

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
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


