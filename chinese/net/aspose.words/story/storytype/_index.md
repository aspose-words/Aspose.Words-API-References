---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: 探索 StoryType 属性，轻松识别和分类您的故事，增强组织能力并改善您的讲故事体验。
type: docs
weight: 40
url: /zh/net/aspose.words/story/storytype/
---
## Story.StoryType property

获取该故事的类型。

```csharp
public StoryType StoryType { get; }
```

## 例子

展示如何从节点中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入形状。这是一个内联形状，
// 它有一个父段落，它是第一节正文的子节点。
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// 我们可以从这个主体的子段落中删除所有形状。
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* enum [StoryType](../../storytype/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
