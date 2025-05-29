---
title: NodeList.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: 使用 GetEnumerator 方法轻松遍历 NodeList。使用 C# 轻松高效地访问节点集合。
type: docs
weight: 30
url: /zh/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

提供对节点集合的简单“foreach”样式迭代。

```csharp
public IEnumerator<Node> GetEnumerator()
```

### 返回值

IEnumerator。

## 例子

展示如何使用 XPath 表达式选择某些节点。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 此表达式将提取所有段落节点，
// 它们是文档中任何表格节点的后代。
NodeList nodeList = doc.SelectNodes("//表格//段落");

// 使用枚举器遍历列表并打印表格中每个单元格中每个段落的内容。
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// 此表达式将选择文档中任何 Body 节点的直接子段落。
nodeList = doc.SelectNodes("//正文/段落”);

// 我们可以将列表视为一个数组。
Assert.AreEqual(4, nodeList.ToArray().Length);

// 使用 SelectSingleNode 选择与上述相同表达式的第一个结果。
Node node = doc.SelectSingleNode("//正文/段落”);

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### 也可以看看

* class [Node](../../node/)
* class [NodeList](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
