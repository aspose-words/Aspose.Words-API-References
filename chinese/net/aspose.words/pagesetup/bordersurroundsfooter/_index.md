---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words for .NET
description: 了解 PageSetup BorderSurroundsFooter 属性如何通过控制页面边框中的页脚包含来增强文档布局。
type: docs
weight: 60
url: /zh/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

指定页面边框是否包含或排除页脚。

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## 评论

注意，更改此属性会影响文档中的所有部分。

## 例子

展示如何为页面和页眉/页脚应用边框。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// 插入蓝色双线边框。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// 一个部分的 PageSetup 对象具有“BorderSurroundsHeader”和“BorderSurroundsFooter”标志，用于确定
// 页面边框是否围绕正文，也分别包括页眉或页脚。
// 将“BorderSurroundsHeader”标志设置为“true”，以用边框围绕标题，
// 然后设置“BorderSurroundsFooter”标志以将页脚留在边框之外。
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
