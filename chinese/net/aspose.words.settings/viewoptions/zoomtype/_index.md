---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words for .NET
description: 探索 ViewOptions ZoomType 属性，根据窗口大小轻松调整缩放级别，增强用户体验和界面灵活性。
type: docs
weight: 60
url: /zh/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

根据窗口大小获取或设置缩放值。

```csharp
public ZoomType ZoomType { get; set; }
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

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
