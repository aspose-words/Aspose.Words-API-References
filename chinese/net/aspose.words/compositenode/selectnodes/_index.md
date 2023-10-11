---
title: CompositeNode.SelectNodes
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 方法. 选择与 XPath 表达式匹配的节点列表
type: docs
weight: 210
url: /zh/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

选择与 XPath 表达式匹配的节点列表。

```csharp
public NodeList SelectNodes(string xpath)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | String | XPath 表达式。 |

### 返回值

与 XPath 查询匹配的节点列表。

### 评论

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式 。

### 例子

演示如何使用 XPath 表达式来测试节点是否位于字段内。

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// 从该 XPath 表达式生成的 NodeList 将包含我们在字段内找到的所有节点。
// 但是，如果路径中存在嵌套字段，FieldStart 和 FieldEnd 节点可以位于列表中。
// 目前未发现FieldCode或FieldResult跨越多个段落的罕见字段。
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// 检查指定的运行是否是字段内的节点之一。
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

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

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


