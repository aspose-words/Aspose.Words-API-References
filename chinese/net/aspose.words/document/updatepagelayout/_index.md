---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words for .NET
description: 使用 UpdatePageLayout 方法修改文档的结构，确保布局精致且井然有序，从而增强可读性和演示效果。
type: docs
weight: 830
url: /zh/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

重建文档的页面布局。

```csharp
public void UpdatePageLayout()
```

## 评论

此方法将文档格式化为页面，并更新文档中与页码相关的字段，例如 PAGE、PAGES、PAGEREF 和 REF。需要最新的页面布局信息才能将 document 正确渲染为固定页面格式。

首次将文档转换为 PDF、XPS、图像或打印时，会自动调用此方法。但是，如果您在渲染后修改文档，然后尝试再次渲染，Aspose.Words 将不会自动更新页面布局。在这种情况下，您应该调用`UpdatePageLayout`before 再次渲染。

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

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
