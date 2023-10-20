---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: 用于 .NET 的 Aspose.Words
description: Node GetText 方法. 获取此节点及其所有子节点的文本 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/node/gettext/
---
## Node.GetText method

获取此节点及其所有子节点的文本。

```csharp
public virtual string GetText()
```

## 评论

返回的字符串包括所有控制字符和特殊字符，如中所述[`ControlChar`](../../controlchar/)。

## 例子

展示如何使用控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入带有文本的段落。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// 将文档转换为文本形式显示控制字符
// 表示文档的一些结构元素，例如分页符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// 将文档转换为字符串形式时，
// 我们可以使用 Trim 方法省略一些控制字符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

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

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
