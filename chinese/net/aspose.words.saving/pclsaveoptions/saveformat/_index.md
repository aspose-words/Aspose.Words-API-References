---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 发现 PclSaveOptions SaveFormat 属性可以轻松地以 PCL 格式保存文档，确保项目的兼容性和高质量输出。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是Pcl.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
