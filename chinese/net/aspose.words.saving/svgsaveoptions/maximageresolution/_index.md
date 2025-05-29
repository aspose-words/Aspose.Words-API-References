---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words for .NET
description: 使用 SvgSaveOptions MaxImageResolution 控制导出光栅图像的质量。设置像素密度以获得最佳效果。默认值为 0。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

获取或设置限制导出光栅图像分辨率的像素/英寸值。默认值为零。

```csharp
public int MaxImageResolution { get; set; }
```

## 评论

如果此属性的值非零，则会限制导出的光栅图像的分辨率。 也就是说，较高分辨率的图像将被重新采样到极限，而较低分辨率的图像将按原样导出。

如果此属性的值为零，则所有光栅图像均会导出而不重新采样。

## 例子

显示如何设置图像分辨率的限制。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### 也可以看看

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
