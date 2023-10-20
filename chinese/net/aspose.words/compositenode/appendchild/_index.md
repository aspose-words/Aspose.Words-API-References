---
title: CompositeNode.AppendChild
linktitle: AppendChild
articleTitle: AppendChild
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode AppendChild 方法. 将指定节点添加到该节点的子节点列表的末尾 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/compositenode/appendchild/
---
## CompositeNode.AppendChild method

将指定节点添加到该节点的子节点列表的末尾。

```csharp
public Node AppendChild(Node newChild)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | Node | 要添加的节点。 |

### 返回值

节点已添加。

## 评论

如果*newChild*已经在树中，首先将其删除。

如果插入的节点是从另一个文档创建的，则应使用 [`ImportNode`](../../documentbase/importnode/)将节点导入到当前文档。 然后可以将导入的节点插入到当前文档中。

## 例子

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

// 一份空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 该文档现在没有可以添加内容的复合子节点。
// 如果我们希望编辑它，我们将需要重新填充它的节点集合。
// 首先，创建一个新节，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 设置该部分的一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个部分需要一个主体，它将包含并显示其所有内容
// 在该部分的页眉和页脚之间的页面上。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子项附加到正文。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后添加一些做文档的内容。创建一个运行，
// 设置其外观和内容，然后将其作为子项附加到段落中。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
