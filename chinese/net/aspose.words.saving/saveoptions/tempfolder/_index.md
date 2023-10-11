---
title: SaveOptions.TempFolder
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹 默认情况下此属性为无效的并且没有使用临时文件
type: docs
weight: 140
url: /zh/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。

```csharp
public string TempFolder { get; set; }
```

### 评论

当Aspose.Words保存文档时，它需要创建临时内部结构。默认情况下， 这些内部结构是在内存中创建的，并且在保存 文档时，内存使用量会在短时间内出现峰值。保存完成后，内存将被释放并由垃圾收集器回收。

如果您正在保存一个非常大的文档（数千页）和/或同时处理许多文档， ，那么保存期间的内存峰值可能足以导致系统抛出异常OutOfMemoryException. 使用指定临时文件夹`TempFolder`将导致Aspose.Words将内部结构保留在 临时文件中而不是内存中。它减少了保存过程中的内存使用量，但会降低保存性能。

该文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

### 例子

演示在保存文档时如何使用硬盘驱动器而不是内存。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们保存文档时，在保存操作发生时，各种元素会临时存储在内存中。
// 我们可以使用此选项来使用本地文件系统中的临时文件夹，
// 这将减少我们应用程序的内存开销。
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// 指定的临时文件夹在保存操作之前必须存在于本地文件系统中。
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// 该文件夹将持续存在，并且加载操作中不会残留任何内容。
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


