---
title: PageSetup.SectionStart
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 返回或设置指定对象的分节符类型
type: docs
weight: 390
url: /zh/net/aspose.words/pagesetup/sectionstart/
---
## PageSetup.SectionStart property

返回或设置指定对象的分节符类型。

```csharp
public SectionStart SectionStart { get; set; }
```

### 例子

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

展示如何指定新部分如何与前一个部分分开。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// 分节符类型决定新节如何与前一节分开。
// 下面是五种类型的分节符。
// 1 - 在新页面上开始下一部分：
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - 开始当前页面的下一部分：
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - 在新的偶数页上开始下一部分：
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - 在新的奇数页上开始下一部分：
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - 在新列上开始下一部分：
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### 也可以看看

* enum [SectionStart](../../sectionstart/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


