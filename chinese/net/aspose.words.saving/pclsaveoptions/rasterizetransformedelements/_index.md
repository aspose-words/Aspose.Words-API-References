---
title: PclSaveOptions.RasterizeTransformedElements
second_title: Aspose.Words for .NET API 参考
description: PclSaveOptions 财产. 获取或设置一个值确定在保存到 PCL 文档之前是否应光栅化复杂的变换元素  默认值为真的.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

获取或设置一个值，确定在保存到 PCL 文档之前是否应光栅化复杂的变换元素 。 默认值为`真的`.

```csharp
public bool RasterizeTransformedElements { get; set; }
```

### 评论

PCL 不支持 Aspose Words 使用的某种转换。 例如旋转、倾斜的图像和纹理画笔。为了正确渲染此类元素 使用光栅化过程，即保存到图像并进行裁剪。 此过程可能需要额外的时间和内存。 如果标志设置为`错误的`，输出中的某些内容可能与源文档不同 。

### 例子

演示如何在将文档保存到 PCL 时对复杂元素进行栅格化。

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
* 命名空间 [Aspose.Words.Saving](../../pclsaveoptions/)
* 部件 [Aspose.Words](../../../)


