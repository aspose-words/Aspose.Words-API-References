---
title: Story.DeleteShapes
second_title: Aspose.Words for .NET API 参考
description: Story 方法. 从这个故事的文本中删除所有形状
type: docs
weight: 70
url: /zh/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

从这个故事的文本中删除所有形状。

```csharp
public void DeleteShapes()
```

### 例子

显示如何从节点中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入一个形状。这是一个内联形状，
// 其中有一个父Paragraph，它是第一节Body的子节点。
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// 我们可以从这个 Body 的子段落中删除所有的形状。
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* class [Story](../)
* 命名空间 [Aspose.Words](../../story/)
* 部件 [Aspose.Words](../../../)


