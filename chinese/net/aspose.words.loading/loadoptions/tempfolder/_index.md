---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: 用于 .NET 的 Aspose.Words
description: LoadOptions TempFolder 财产. 允许在读取文档时使用临时文件 默认情况下此属性为无效的并且没有使用临时文件 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

允许在读取文档时使用临时文件。 默认情况下，此属性为`无效的`并且没有使用临时文件。

```csharp
public string TempFolder { get; set; }
```

## 评论

文件夹必须存在且可写，否则会抛出异常。

读取完成后，Aspose.Words 会自动删除所有临时文件。

## 例子

显示如何使用临时文件加载文档。

```csharp
// 请注意，这种方法可以减少内存使用但会降低速度
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// 确保目录存在并加载
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

显示加载文档时如何使用硬盘驱动器而不是内存。

```csharp
// 当我们加载一个文档时，随着保存操作的发生，各种元素会临时存储在内存中。
// 我们可以使用此选项来使用本地文件系统中的临时文件夹，
// 这将减少我们应用程序的内存开销。
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// 在加载操作之前，指定的临时文件夹必须存在于本地文件系统中。
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// 该文件夹将持久保存，没有来自加载操作的残留内容。
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
