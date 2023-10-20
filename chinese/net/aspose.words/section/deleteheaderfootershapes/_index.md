---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: 用于 .NET 的 Aspose.Words
description: Section DeleteHeaderFooterShapes 方法. 删除本节页眉和页脚中的所有形状绘图对象 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

删除本节页眉和页脚中的所有形状（绘图对象）。

```csharp
public void DeleteHeaderFooterShapes()
```

## 例子

演示如何从节中的所有页眉页脚中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个带有形状的主标题。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// 使用图像创建主页脚。
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo Icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// 从第一部分的页眉和页脚中删除所有形状。
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
