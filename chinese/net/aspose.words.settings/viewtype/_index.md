---
title: ViewType Enum
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words for .NET
description: 探索适用于 Microsoft Word 的 Aspose.Words.Settings.ViewType 枚举。解锁灵活的视图模式，增强文档呈现效果和用户体验。
type: docs
weight: 6790
url: /zh/net/aspose.words.settings/viewtype/
---
## ViewType enumeration

Microsoft Word 中视图模式的可能值。

```csharp
public enum ViewType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 该文档应在应用程序的默认视图中呈现。 |
| Reading | `0` | 该文档应在应用程序的默认视图中呈现。 |
| PageLayout | `1` | 文档应在显示打印文档的视图中打开。 |
| Outline | `3` | 该文档应在针对概述或创建长文档而优化的视图中呈现。 |
| Normal | `4` | 该文档应在针对概述或创建长文档而优化的视图中呈现。 |
| Web | `5` | 该文档应以与网页中显示方式相同的视图呈现。 |

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

* class [ViewOptions](../viewoptions/)
* property [ViewType](../viewoptions/viewtype/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
