---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words for .NET
description: 调整 ViewOptions 的 ZoomPercent 属性，将文档的缩放级别设置为 10-500%。增强可读性并优化您的观看体验！
type: docs
weight: 50
url: /zh/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

获取或设置您想要查看文档的百分比。

```csharp
public int ZoomPercent { get; set; }
```

## 评论

尽管 Aspose.Words 能够读取和写入此选项，但其用法是特定于应用程序的。 例如，MS Word 2013 不尊重此选项的值。

## 例子

展示如何设置自定义缩放比例，旧版本的 Microsoft Word 将在加载时将该比例应用于文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### 也可以看看

* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
