---
title: ViewType
second_title: Aspose.Words for .NET API 参考
description: 控制 Microsoft Word 中的查看模式
type: docs
weight: 40
url: /zh/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

控制 Microsoft Word 中的查看模式。

```csharp
public ViewType ViewType { get; set; }
```

### 评论

虽然 Aspose.Words 能够读写这个选项，但它的使用是特定于应用程序的。 例如 MS Word 2013 不尊重此选项的值。

### 例子

显示如何设置自定义缩放系数，旧版本的 Microsoft Word 将在加载时应用于文档。

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

* enum [ViewType](../../viewtype)
* class [ViewOptions](../../viewoptions)
* 命名空间 [Aspose.Words.Settings](../../viewoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->