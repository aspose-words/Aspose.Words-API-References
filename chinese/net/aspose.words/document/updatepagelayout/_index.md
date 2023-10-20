---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: 用于 .NET 的 Aspose.Words
description: Document UpdatePageLayout 方法. 重建文档的页面布局 在 C#.
type: docs
weight: 770
url: /zh/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

重建文档的页面布局。

```csharp
public void UpdatePageLayout()
```

## 评论

此方法将文档格式化为页面，并更新文档中与页码相关的字段，如 PAGE、PAGES、PAGEREF 和 REF。将 document 正确呈现为固定页面格式需要最新的页面布局信息。

当您第一次将文档转换为 PDF、XPS、图像或打印时，会自动调用此方法。 但是，如果您在渲染后修改文档，然后尝试再次渲染它 - Aspose.Words 将不会 自动更新页面布局。在这种情况下你应该打电话`UpdatePageLayout`before 再次渲染。

## 例子

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

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
