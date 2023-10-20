---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: 用于 .NET 的 Aspose.Words
description: Story DeleteShapes 方法. 删除此故事文本中的所有形状 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

删除此故事文本中的所有形状。

```csharp
public void DeleteShapes()
```

## 例子

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

* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
