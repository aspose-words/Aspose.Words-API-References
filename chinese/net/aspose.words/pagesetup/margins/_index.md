---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words for .NET
description: 使用 PageSetup 属性轻松调整页面边距。自定义设置以获得最佳布局和显示效果。提升文档外观！
type: docs
weight: 260
url: /zh/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

返回或设置预设[`Margins`](../../margins/)页面的。

```csharp
public Margins Margins { get; set; }
```

## 例子

显示何时重新计算文档的页面布局。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 将文档保存为 PDF、图像或首次打印时将自动
// 在文档的页面内缓存其布局。
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// 在当前版本的 Aspose.Words 中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望使用缓存的布局
// 为了保持最新状态，我们需要手动更新它。
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### 也可以看看

* enum [Margins](../../margins/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
