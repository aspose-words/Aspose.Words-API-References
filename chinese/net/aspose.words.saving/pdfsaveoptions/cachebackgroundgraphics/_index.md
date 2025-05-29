---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions CacheBackgroundGraphics 属性以优化文档图形缓存，增强 PDF 创建和性能。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

获取或设置一个值，确定是否缓存放置在文档背景中的图形。

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## 评论

默认值为`真的`并将背景图形作为 xObject 写入 PDF 文档。

当值为`错误的`背景图形未被缓存。

某些形状不支持缓存（带有字段、书签、HRefs 的形状）。

文档背景图形是放置在页脚或页眉中的各种形状、图表、图像以及页面的背景和边框。

## 例子

显示如何缓存放置在文档背景中的图形。

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
