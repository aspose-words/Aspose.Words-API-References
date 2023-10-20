---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: 用于 .NET 的 Aspose.Words
description: Body ParentSection 财产. 获取此故事的父部分 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

获取此故事的父部分。

```csharp
public Section ParentSection { get; }
```

## 评论

`ParentSection`相当于[`ParentNode`](../../node/parentnode/)投射到[`Section`](../../section/)。

## 例子

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

* class [Section](../../section/)
* class [Body](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
