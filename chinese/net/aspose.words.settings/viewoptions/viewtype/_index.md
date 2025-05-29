---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: 探索 ViewOptions ViewType 属性，轻松自定义 Microsoft Word 视图模式，从而提高工作效率并获得量身定制的编辑体验。
type: docs
weight: 40
url: /zh/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

控制 Microsoft Word 中的视图模式。

```csharp
public ViewType ViewType { get; set; }
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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
