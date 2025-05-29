---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: Aspose.Words for .NET
description: 了解 PageSetup SuppressEndnotes 属性如何通过控制尾注位置来增强文档布局，从而使各个部分更加清晰、有条理。
type: docs
weight: 410
url: /zh/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

如果尾注打印在下一节的末尾，且该节不抑制尾注，则为真。 抑制的尾注将打印在该节的尾注之前。

```csharp
public bool SuppressEndnotes { get; set; }
```

## 例子

展示如何在每节末尾存储尾注，并修改其位置。

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // 默认情况下，文档会在末尾编译所有尾注。
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // 我们使用文档“EndnoteOptions”对象的“Position”属性
    // 而是在每个部分的末尾收集尾注。
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // 在让各部分显示各自的尾注时，我们可以设置“SuppressEndnotes”标志
    // 将章节的“PageSetup”对象设置为“true”，以恢复默认行为并传递其尾注
    // 进入下一部分。
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// 将包含文本和尾注的部分附加到文档。
/// </summary>
private static void InsertSectionWithEndnote(Document doc, string sectionBodyText, string endnoteText)
{
    Section section = new Section(doc);

    doc.AppendChild(section);

    Body body = new Body(doc);
    section.AppendChild(body);

    Assert.AreEqual(section, body.ParentNode);

    Paragraph para = new Paragraph(doc);
    body.AppendChild(para);

    Assert.AreEqual(body, para.ParentNode);

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.MoveTo(para);
    builder.Write(sectionBodyText);
    builder.InsertFootnote(FootnoteType.Endnote, endnoteText);
}
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
