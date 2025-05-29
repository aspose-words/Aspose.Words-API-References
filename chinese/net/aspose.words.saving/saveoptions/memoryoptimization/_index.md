---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words for .NET
description: 使用 SaveOptions MemoryOptimization 属性增强文档性能。在保存前控制内存使用量，提高效率和速度。
type: docs
weight: 100
url: /zh/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为`错误的`.

```csharp
public bool MemoryOptimization { get; set; }
```

## 评论

将此选项设置为`真的`可以显著减少内存消耗，同时保存大型文档，但保存时间会变慢。

## 例子

显示在将大型文档呈现为 PDF 时优化内存消耗的选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// 将“MemoryOptimization”属性设置为“true”以降低大文档保存操作的内存占用
// 代价是增加操作的持续时间。
// 将“MemoryOptimization”属性设置为“false”以正常将文档保存为 PDF。
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
