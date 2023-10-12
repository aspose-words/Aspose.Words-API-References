---
title: PageSetup.SuppressEndnotes
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 如果尾注打印在下一个不抑制尾注的部分的末尾则为 True 抑制的尾注将在该部分中的尾注之前打印
type: docs
weight: 410
url: /zh/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

如果尾注打印在下一个不抑制尾注的部分的末尾，则为 True。 抑制的尾注将在该部分中的尾注之前打印。

```csharp
public bool SuppressEndnotes { get; set; }
```

### 例子

展示如何在每个部分的末尾存储尾注并修改它们的位置。

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // 默认情况下，文档在其末尾编译所有尾注。
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // 我们使用文档的“EndnoteOptions”对象的“Position”属性
    // 在每个部分的末尾收集尾注。
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // 在让节显示各自的尾注时，我们可以设置“SuppressEndnotes”标志
    // 将某个部分的“PageSetup”对象设置为“true”以恢复默认行为并传递其尾注
    // 进入下一节。
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// 将包含文本和尾注的部分附加到文档中。
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
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


