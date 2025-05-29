---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用 NodeList Item 属性轻松访问特定节点。通过索引检索节点，简化数据操作并提高编码效率。
type: docs
weight: 20
url: /zh/net/aspose.words/nodelist/item/
---
## NodeList indexer

检索给定索引处的节点。

```csharp
public Node this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 节点列表的索引。 |

## 评论

该索引从零开始。

允许使用负索引，表示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负数并且其绝对值大于列表中的项目数，则返回空引用。

## 例子

展示如何使用 XPath 导航 NodeList。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入一些节点。
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// 我们的文档包含三个 Run 节点。
NodeList nodeList = doc.SelectNodes("//跑步”）;

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// 使用双斜杠选择所有 Run 节点
// 它们是表节点的间接后代，也就是我们插入的两个单元格内的运行。
nodeList = doc.SelectNodes("//Table//跑步”）;

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// 单斜杠指定直接后代关系，
// 当我们使用双斜杠时我们跳过了它。
Assert.AreEqual(doc.SelectNodes(" //表//运行”），
    doc.SelectNodes("//表格/行/单元格/段落/运行”））；

// 访问包含我们插入的图像的形状。
nodeList = doc.SelectNodes("//形状”）;

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### 也可以看看

* class [Node](../../node/)
* class [NodeList](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
