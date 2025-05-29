---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words for .NET
description: 使用 SaveOptions TempFolder 属性优化文档保存，该属性指定一个用于临时 DOC 和 DOCX 文件的文件夹，从而提高效率。
type: docs
weight: 140
url: /zh/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

指定保存为 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且不使用临时文件。

```csharp
public string TempFolder { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| OutOfMemoryException | 如果您正在保存非常大的文档（数千页）和/或同时处理许多文档，则会抛出该异常。 保存期间的内存峰值可能足够大，从而导致异常。 |

## 评论

Aspose.Words 保存文档时，需要创建临时的内部结构。默认情况下，这些内部结构会在内存中创建，并且在保存文档时，内存使用量会在短时间内达到峰值。保存完成后，内存将被释放并由垃圾回收器回收。

使用指定临时文件夹`TempFolder`这将导致 Aspose.Words 将内部结构保存在临时文件中，而不是内存中。这可以减少保存期间的内存使用量，但会降低保存性能。

该文件夹必须存在且可写，否则将引发异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

## 例子

展示如何在保存文档时使用硬盘而不是内存。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们保存文档时，各种元素会在保存操作进行时暂时存储在内存中。
// 我们可以使用此选项来使用本地文件系统中的临时文件夹，
//这将减少我们应用程序的内存开销。
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// 保存操作之前，指定的临时文件夹必须存在于本地文件系统中。
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// 该文件夹将保留，不会留下加载操作留下的任何内容。
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
