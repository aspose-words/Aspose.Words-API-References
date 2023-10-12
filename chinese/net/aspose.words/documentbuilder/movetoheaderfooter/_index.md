---
title: DocumentBuilder.MoveToHeaderFooter
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将光标移动到当前节中页眉或页脚的开头
type: docs
weight: 550
url: /zh/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

将光标移动到当前节中页眉或页脚的开头。

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | 指定要移动到的页眉或页脚。 |

### 评论

将光标移至页眉或页脚后，您可以使用其余部分[`DocumentBuilder`](../) 修改页眉或页脚内容的方法。

如果你想为第一页创建不同的页眉和页脚，你需要 来设置[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/)。

如果要为偶数页和奇数页创建不同的页眉和页脚，则需要 来设置[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/)。

使用[`MoveToSection`](../movetosection/)从标题移到正文中。

### 例子

演示如何插入图像并将其用作水印。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将图像插入页眉中，以便它在每个页面上都可见。
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// 将图像放置在页面的中心。
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

演示如何插入图像并将其用作水印 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将图像插入页眉中，以便它在每个页面上都可见。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // 将图像放置在页面的中心。
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

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

### 也可以看看

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


