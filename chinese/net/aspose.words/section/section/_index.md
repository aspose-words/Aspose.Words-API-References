---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words for .NET
description: 使用我们的 Section 构造器轻松创建动态 Web 部分。轻松初始化和自定义您的 Section 类，以获得最佳网站性能。
type: docs
weight: 10
url: /zh/net/aspose.words/section/section/
---
## Section constructor

初始化 Section 类的新实例。

```csharp
public Section(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

## 评论

当该部分被创建时，它属于指定的文档，但还不是文档的一部分，并且[`ParentNode`](../../node/parentnode/)是`无效的`。

包括[`Section`](../)进入文档使用[`InsertAfter`](../../compositenode/insertafter/)和 [`InsertBefore`](../../compositenode/insertbefore/)方法[`Document`](../../document/)或 [`Add`](../../nodecollection/add/)和[`Insert`](../../nodecollection/insert/)方法[`Sections`](../../document/sections/)财产。

## 例子

展示如何手动构建 Aspose.Words 文档。

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

// 为该部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个部分需要一个主体，它将包含并显示其所有内容
// 位于页面部分页眉和页脚之间。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子部分附加到正文中。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后，添加一些内容来执行文档。创建一个运行，
// 设置其外观和内容，然后将其作为子项附加到段落。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
