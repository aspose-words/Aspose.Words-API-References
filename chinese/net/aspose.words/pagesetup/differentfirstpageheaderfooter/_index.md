---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: Aspose.Words for .NET
description: 探索 PageSetup DifferentFirstPageHeaderFooter 属性，使用独特的页眉和页脚自定义文档的第一页，以获得专业的感觉。
type: docs
weight: 110
url: /zh/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

如果第一页使用不同的页眉或页脚，则为真。

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## 例子

展示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望第一页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建页眉，然后向文档添加三页以显示每种页眉类型。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

显示如何启用或禁用主页眉/页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种类型的页眉/页脚。
// 1 - “第一”页眉/页脚，出现在该部分的第一页上。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - “主要”页眉/页脚，出现在该部分的每一页上。
// 我们可以通过第一页和偶数页的页眉/页脚覆盖主页眉/页脚。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 每个部分都有一个“PageSetup”对象，用于指定与页面外观相关的属性
// 例如方向、大小和边框。
// 将“DifferentFirstPageHeaderFooter”属性设置为“true”，以将第一个页眉/页脚应用于第一页。
// 将“DifferentFirstPageHeaderFooter”属性设置为“false”
// 使第一页显示主页眉/页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

展示如何跟踪文本替换操作遍历节点的顺序。

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // 对第一页使用不同的页眉/页脚将影响搜索顺序。
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// 在查找和替换操作期间，记录操作“找到”的每个包含文本的节点的内容，
/// 处于替换发生之前的状态。
/// 这将显示文本替换操作遍历节点的顺序。
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
