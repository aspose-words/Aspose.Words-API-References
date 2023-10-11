---
title: Story.StoryType
second_title: Aspose.Words for .NET API 参考
description: Story 财产. 获取此故事的类型
type: docs
weight: 40
url: /zh/net/aspose.words/story/storytype/
---
## Story.StoryType property

获取此故事的类型。

```csharp
public StoryType StoryType { get; }
```

### 例子

演示如何从节点中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入形状。这是一个内嵌的形状，
// 它有一个父 Paragraph，它是第一个部分的 Body 的子节点。
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// 我们可以从该 Body 的子段落中删除所有形状。
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* enum [StoryType](../../storytype/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../story/)
* 部件 [Aspose.Words](../../../)


