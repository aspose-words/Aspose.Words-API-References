---
title: SaveOptions.MemoryOptimization
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 获取或设置确定在保存文档之前是否应执行内存优化的值 此属性的默认值为错误的.
type: docs
weight: 100
url: /zh/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

获取或设置确定在保存文档之前是否应执行内存优化的值。 此属性的默认值为`错误的`.

```csharp
public bool MemoryOptimization { get; set; }
```

### 评论

将此选项设置为`真的`可以显着减少内存消耗，同时保存大型文档，但代价是保存时间较慢。

### 例子

显示将大型文档渲染为 PDF 时优化内存消耗的选项。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// 将“MemoryOptimization”属性设置为“true”以降低大文档保存操作的内存占用
// 以增加操作持续时间为代价。
// 将“MemoryOptimization”属性设置为“false”以正常将文档保存为 PDF。
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


