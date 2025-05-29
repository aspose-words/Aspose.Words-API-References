---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.CompressionLevel 枚举以优化 OOXML 文件大小，提高文档处理的性能和效率。
type: docs
weight: 5610
url: /zh/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

OOXML 文件的压缩级别。

（DOCX 和 DOTX 文件在内部是 ZIP 档案，此属性控制档案的压缩级别。

请注意，FlatOpc 文件不是 ZIP 存档，因此，此属性不会影响 FlatOpc 文件。)

```csharp
public enum CompressionLevel
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Normal | `0` | 正常压缩级别。Aspose.Words 使用的默认压缩级别。 |
| Maximum | `1` | 最大压缩级别。 |
| Fast | `2` | 快速压缩级别。 |
| SuperFast | `3` | 超快压缩级别。Microsoft Word 使用此压缩级别。 |

## 例子

展示如何指定保存 OOXML 文档时使用的压缩级别。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// 当我们将文档保存为 OOXML 格式时，我们可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法来修改我们保存文档的方式。
// 将“CompressionLevel”属性设置为“CompressionLevel.Maximum”以应用最强和最慢的压缩。
// 将“CompressionLevel”属性设置为“CompressionLevel.Normal”以应用
// Aspose.Words 在保存 OOXML 文档时使用的默认压缩。
// 将“CompressionLevel”属性设置为“CompressionLevel.Fast”以应用更快、更弱的压缩。
// 将“CompressionLevel”属性设置为“CompressionLevel.SuperFast”以应用
// Microsoft Word 使用的默认压缩。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
