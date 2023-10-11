---
title: OoxmlSaveOptions.CompressionLevel
second_title: Aspose.Words for .NET API 参考
description: OoxmlSaveOptions 财产. 指定用于保存文档的压缩级别 默认值为Normal.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

指定用于保存文档的压缩级别。 默认值为Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### 例子

演示如何指定保存 OOXML 文档时要使用的压缩级别。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// 当我们将文档保存为 OOXML 格式时，我们可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法来修改我们保存文档的方式。
// 将“ CompressionLevel”属性设置为“ CompressionLevel.Maximum”以应用最强和最慢的压缩。
// 将“CompressionLevel”属性设置为“CompressionLevel.Normal”以应用
// Aspose.Words 在保存 OOXML 文档时使用的默认压缩。
// 将“压缩级别”属性设置为“压缩级别.快速”以应用更快且更弱的压缩。
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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


