---
title: NodeList.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: NodeList 方法. 在节点集合上提供简单的foreach样式迭代
type: docs
weight: 30
url: /zh/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

在节点集合上提供简单的“foreach”样式迭代。

```csharp
public IEnumerator<Node> GetEnumerator()
```

### 返回值

一个 IEnumerator。

### 例子

显示如何使用 XPath 表达式选择某些节点。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 这个表达式将提取所有段落节点，
// 它们是文档中任何表节点的后代。
NodeList nodeList = doc.SelectNodes("//表格//段落");

// 使用枚举器遍历列表并打印表格每个单元格中每个段落的内容。
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// 此表达式将选择作为文档中任何 Body 节点的直接子级的任何段落。
nodeList = doc.SelectNodes("//正文/段落");

// 我们可以将列表视为一个数组。
Assert.AreEqual(4, nodeList.ToArray().Length);

// 使用 SelectSingleNode 选择与上面相同表达式的第一个结果。
Node node = doc.SelectSingleNode("//正文/段落");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### 也可以看看

* class [Node](../../node/)
* class [NodeList](../)
* 命名空间 [Aspose.Words](../../nodelist/)
* 部件 [Aspose.Words](../../../)


