---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ParagraphAlignment 枚举. 指定段落中的文本对齐方式 在 C#.
type: docs
weight: 4400
url: /zh/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

指定段落中的文本对齐方式。

```csharp
public enum ParagraphAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Left | `0` | 文本左对齐。 |
| Center | `1` | 文本水平居中。 |
| Right | `2` | 文本右对齐。 |
| Justify | `3` | 文本左右对齐。 |
| Distributed | `4` | 文本均匀分布。 |
| ArabicMediumKashida | `5` | 仅阿拉伯语。文本的 Kashida 长度扩展为由消费者确定的中等长度。 |
| ArabicHighKashida | `7` | 仅阿拉伯语。文本的 Kashida 长度已扩展至尽可能宽的长度。 |
| ArabicLowKashida | `8` | 仅阿拉伯语。文本的 Kashida 长度延长为稍长的长度。 |
| ThaiDistributed | `9` | 仅泰语。通过对泰语的优化来调整文本。 |
| MathElementCenterAsGroup | `10` | 一行中唯一的数学元素，对齐为“居中为组”。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
