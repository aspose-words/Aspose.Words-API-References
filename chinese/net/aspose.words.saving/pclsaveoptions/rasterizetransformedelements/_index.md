---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words for .NET
description: 使用 PclSaveOptions 控制 PCL 文档中复杂元素的光栅化。轻松管理图像质量和文件大小，以获得最佳效果。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

获取或设置一个值，确定在保存到 PCL 文档之前是否应将复杂转换元素 光栅化。 默认值为`真的`.

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## 评论

PCL 不支持 Aspose Words 使用的某些类型的转换。 例如旋转、倾斜的图像和纹理画笔。为了正确渲染这些元素， 需要使用光栅化处理，即保存到图像并进行裁剪。 此过程可能需要额外的时间和内存。 如果标志设置为`错误的`，输出中的某些内容可能与源文档不同 。

## 例子

展示如何在将文档保存为 PCL 时光栅化复杂元素。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### 也可以看看

* class [PclSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
