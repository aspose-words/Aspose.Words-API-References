---
title: Document.FirstSection
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 获取文档中的第一部分
type: docs
weight: 130
url: /zh/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

获取文档中的第一部分。

```csharp
public Section FirstSection { get; }
```

### 评论

返回`无效的`如果没有部分.

### 例子

演示如何替换文档页脚中的文本。

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

演示如何使用文档生成器创建新部分。

```csharp
Document doc = new Document();

// 空白文档默认包含一个部分，
// 其中包含我们可以编辑的子节点。
Assert.AreEqual(1, doc.Sections.Count);

// 使用文档生成器将文本添加到第一部分。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 通过插入分节符创建第二部分。
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// 每个部分都有自己的页面设置。
// 我们可以将第二部分中的文本分成两列。
// 这不会影响第一部分中的文本。
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

演示如何迭代复合节点的子节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// 一个Section是一个复合节点并且可以包含子节点，
// 但前提是这些子节点属于“Body”或“HeaderFooter”节点类型。
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### 也可以看看

* class [Section](../../section/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


