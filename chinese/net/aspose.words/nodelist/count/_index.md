---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 发现 NodeList Count 属性可以轻松检索列表中的节点总数，从而提高 Web 开发效率。
type: docs
weight: 10
url: /zh/net/aspose.words/nodelist/count/
---
## NodeList.Count property

获取列表中的节点数。

```csharp
public int Count { get; }
```

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

* class [NodeList](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
