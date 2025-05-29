---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: 使用 Body EnsureMinimum 方法优化您的内容。如果最后一个子元素不是段落，则自动添加一个空段落，以实现更佳的格式。
type: docs
weight: 70
url: /zh/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

如果最后一个子项不是段落，则创建并附加一个空段落。

```csharp
public void EnsureMinimum()
```

## 例子

清除文档所有章节的正文，只留下章节本身。

```csharp
Document doc = new Document();

// 一个空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法删除所有节点，
// 并最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 此文档现在没有可以添加内容的复合子节点。
// 如果我们想要编辑它，我们将需要重新填充它的节点集合。
// 首先，创建一个新的部分，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 一个部分需要一个主体，它将包含并显示其所有内容
// 位于页面部分页眉和页脚之间。
Body body = new Body(doc);
section.AppendChild(body);

// 这个主体没有子主体，所以我们还不能为其添加运行。
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // 调用“EnsureMinimum”以确保此正文至少包含一个空段落。
body.EnsureMinimum();

// 现在，我们可以将运行添加到正文中，并获取文档来显示它们。
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [Body](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
