---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup BorderSurroundsFooter 财产. 指定页面边框是包含还是排除页脚 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

指定页面边框是包含还是排除页脚。

```csharp
public bool BorderSurroundsFooter { get; set; }
```

## 评论

注意，更改此属性会影响文档中的所有部分。

## 例子

演示如何将边框应用到页面和页眉/页脚。

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

// 一个section的PageSetup对象有“BorderSurroundsHeader”和“BorderSurroundsFooter”标志来确定
// 页面边框是否包围主体文本，还分别包括页眉或页脚。
// 将“BorderSurroundsHeader”标志设置为“true”以用边框包围标题，
// 然后设置“BorderSurroundsFooter”标志将页脚保留在边框之外。
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### 也可以看看

* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
