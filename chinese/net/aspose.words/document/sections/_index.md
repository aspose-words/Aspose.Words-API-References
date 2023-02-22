---
title: Document.Sections
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 返回代表文档中所有部分的集合
type: docs
weight: 350
url: /zh/net/aspose.words/document/sections/
---
## Document.Sections property

返回代表文档中所有部分的集合。

```csharp
public SectionCollection Sections { get; }
```

### 例子

显示如何在文档中添加和删除部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// 从文档中删除第一部分。
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// 将现在第一部分的副本附加到文档的末尾。
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

显示如何指定新部分如何与前一个部分分开。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// 分节符类型决定了新节如何将自己与前一节分开。
// 下面是五种分节符。
// 1 - 在新页面上开始下一节：
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - 开始当前页面的下一部分：
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - 在新的偶数页上开始下一节：
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - 在新奇数页上开始下一节：
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - 在新列上开始下一节：
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### 也可以看看

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


