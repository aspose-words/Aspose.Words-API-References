---
title: ZoomType Enum
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.ZoomType 枚举以自定义 Microsoft Word 中的文档显示大小，从而实现最佳查看效果和工作效率。
type: docs
weight: 6810
url: /zh/net/aspose.words.settings/zoomtype/
---
## ZoomType enumeration

Microsoft Word 中文档在屏幕上显示的大小可能值。

```csharp
public enum ZoomType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Custom | `0` | 缩放百分比已明确设置。控件大小发生变化时，不会自动重新计算。 |
| None | `0` | 表示使用明确的缩放百分比。与Custom. |
| FullPage | `1` | 缩放百分比会自动重新计算以适合整页。 |
| PageWidth | `2` | 缩放百分比会自动重新计算以适应页面宽度。 |
| TextFit | `3` | 缩放百分比会自动重新计算以适合文本。 |

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
* property [ZoomType](../viewoptions/zoomtype/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
