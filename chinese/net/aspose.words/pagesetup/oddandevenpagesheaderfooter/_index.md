---
title: PageSetup.OddAndEvenPagesHeaderFooter
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 如果文档的奇数页和偶数页具有不同的页眉和页脚则为 True
type: docs
weight: 280
url: /zh/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

如果文档的奇数页和偶数页具有不同的页眉和页脚，则为 True。

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

### 评论

注意，更改此属性会影响文档中的所有部分。

### 例子

演示如何使用 DocumentBuilder 在文档中创建页眉和页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定我们希望首页、偶数页和奇数页使用不同的页眉和页脚。
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// 创建标题，然后向文档添加三个页面以显示每种标题类型。
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

显示如何启用或禁用页眉/页脚。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是两种类型的页眉/页脚。
// 1 - “主要”页眉/页脚，出现在该部分的每个页面上。
 // 我们可以用第一个和偶数页页眉/页脚覆盖主页眉/页脚。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - “偶数”页眉/页脚，出现在本节的每个偶数页上。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 每个部分都有一个“PageSetup”对象，用于指定页面外观相关的属性
// 例如方向、大小和边框。
// 将“OddAndEvenPagesHeaderFooter”属性设置为“true”
// 在偶数页上显示偶数页页眉/页脚。
// 将“OddAndEvenPagesHeaderFooter”属性设置为“false”
// 在偶数页上显示主页眉/页脚。
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


