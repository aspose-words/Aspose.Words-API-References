---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words for .NET
description: 使用 MergeToImages 方法轻松合并多个文档，创建单个图像输出，同时自定义文件名和保存选项。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 将输出呈现为图像。

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFiles | String[] | 输入文件名。 |
| saveOptions | ImageSaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

使用指定的图像保存选项将给定的输入文档流合并为单个输出文档。 将输出呈现为图像。

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStreams | Stream[] | 输入文件流。 |
| saveOptions | ImageSaveOptions | 保存选项。 |
| mergeFormatMode | MergeFormatMode | 指定如何合并冲突的格式。 |

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
