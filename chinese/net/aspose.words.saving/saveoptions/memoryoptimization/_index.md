---
title: SaveOptions.MemoryOptimization
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 获取或设置值确定是否应在保存文档之前执行内存优化 此属性的默认值为 错误的.
type: docs
weight: 110
url: /zh/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

获取或设置值确定是否应在保存文档之前执行内存优化。 此属性的默认值为 **错误的**.

```csharp
public bool MemoryOptimization { get; set; }
```

### 评论

将此选项设置为 true 可以显着减少内存消耗，同时以较慢的节省时间为代价保存大型文档。

### 例子

显示在将大型文档呈现为 PDF 时优化内存消耗的选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// 将“MemoryOptimization”属性设置为“true”以降低大型文档保存操作的内存占用
// 以增加操作的持续时间为代价。
// 将“MemoryOptimization”属性设置为“false”以正常将文档保存为PDF。
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


