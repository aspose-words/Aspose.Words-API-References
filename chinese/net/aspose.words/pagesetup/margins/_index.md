---
title: PageSetup.Margins
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 返回或设置预设Margins页面的大小.
type: docs
weight: 260
url: /zh/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

返回或设置预设[`Margins`](../../margins/)页面的大小.

```csharp
public Margins Margins { get; set; }
```

### 例子

显示何时重新计算文档的页面布局。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 第一次将文档保存为 PDF、图像或打印
// 在其页面中缓存文档的布局。
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // 在当前版本的Aspose.Words中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存布局
// 为了保持最新状态，我们需要手动更新它。
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### 也可以看看

* enum [Margins](../../margins/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


