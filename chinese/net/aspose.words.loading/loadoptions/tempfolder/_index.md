---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words for .NET
description: 使用 LoadOptions 的 TempFolder 属性优化文档读取。轻松管理临时文件，实现高效处理并提升性能。
type: docs
weight: 150
url: /zh/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

允许在读取文档时使用临时文件。 默认情况下，此属性为`无效的`并且不使用临时文件。

```csharp
public string TempFolder { get; set; }
```

## 评论

该文件夹必须存在且可写，否则将引发异常。

读取完成后，Aspose.Words 会自动删除所有临时文件。

## 例子

展示如何使用临时文件加载文档。

```csharp
// 注意，这种方法可以减少内存使用，但会降低速度
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// 确保目录存在并加载
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

展示如何在加载文档时使用硬盘而不是内存。

```csharp
// 当我们加载文档时，各种元素会在保存操作发生时暂时存储在内存中。
// 我们可以使用此选项来使用本地文件系统中的临时文件夹，
//这将减少我们应用程序的内存开销。
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// 加载操作之前，指定的临时文件夹必须存在于本地文件系统中。
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// 该文件夹将保留，不会留下加载操作留下的任何内容。
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
