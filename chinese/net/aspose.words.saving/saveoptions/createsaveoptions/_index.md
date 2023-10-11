---
title: SaveOptions.CreateSaveOptions
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 方法. 创建适合指定保存格式的类的保存选项对象
type: docs
weight: 10
url: /zh/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

创建适合指定保存格式的类的保存选项对象。

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | SaveFormat | 要为其创建保存选项对象的保存格式。 |

### 返回值

派生自的类的对象[`SaveOptions`](../)。

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

创建适合给定文件名中指定的文件扩展名的类的保存选项对象。

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 该文件名的扩展名决定了要创建的保存选项对象的类。 |

### 返回值

派生自的类的对象[`SaveOptions`](../)。

### 例子

演示如何为没有附加模板的文档设置默认模板。

```csharp
Document doc = new Document();

// 启用自动样式更新，但不附加模板文档。
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// 由于没有模板文档，文档无处跟踪样式更改。
// 使用 SaveOptions 对象自动设置模板
// 如果我们正在保存的文档没有该文档。
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


