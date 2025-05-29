---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words for .NET
description: 发现文档 ViewOptions 属性以自定义 Microsoft Word 显示设置，以获得定制的查看体验。
type: docs
weight: 490
url: /zh/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

提供选项来控制文档在 Microsoft Word 中的显示方式。

```csharp
public ViewOptions ViewOptions { get; }
```

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

展示如何设置自定义缩放类型，旧版本的 Microsoft Word 将在加载时将其应用于文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 将“ZoomType”属性设置为“ZoomType.PageWidth”以获取 Microsoft Word
// 自动缩放文档以适合页面的宽度。
// 将“ZoomType”属性设置为“ZoomType.FullPage”以获取 Microsoft Word
// 自动缩放文档以使整个第一页可见。
// 将“ZoomType”属性设置为“ZoomType.TextFit”以获取 Microsoft Word
// 自动缩放文档以适合第一页的内部文本边距。
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### 也可以看看

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
