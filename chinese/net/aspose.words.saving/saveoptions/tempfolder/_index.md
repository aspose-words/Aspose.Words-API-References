---
title: SaveOptions.TempFolder
second_title: Aspose.Words for .NET API 参考
description: SaveOptions 财产. 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹 默认情况下此属性为无效的并且没有使用临时文件
type: docs
weight: 150
url: /zh/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。

```csharp
public string TempFolder { get; set; }
```

### 评论

当 Aspose.Words 保存文档时，它需要创建临时的内部结构。默认情况下， 这些内部结构是在内存中创建的，当 文档被保存时，内存使用量会在短时间内达到峰值。保存完成后，内存将被垃圾收集器释放和回收。

如果您要保存一个非常大的文档（数千页）和/或同时处理许多文档， 则保存期间的内存峰值可能足以导致系统抛出OutOfMemoryException. 使用指定临时文件夹`TempFolder`将导致 Aspose.Words 将内部结构保存在 临时文件而不是内存中。它会减少保存期间的内存使用量，但会降低保存性能。

文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

### 例子

显示保存文档时如何使用硬盘驱动器而不是内存。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们保存一个文档时，各种元素会在保存操作发生时临时存储在内存中。
// 我们可以使用此选项来使用本地文件系统中的临时文件夹，
// 这将减少我们应用程序的内存开销。
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// 指定的临时文件夹在保存操作前必须存在于本地文件系统中。
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// 该文件夹将持久保存，没有来自加载操作的残留内容。
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../saveoptions/)
* 部件 [Aspose.Words](../../../)


