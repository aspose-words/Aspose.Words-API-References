---
title: DocSaveOptions.AlwaysCompressMetafiles
second_title: Aspose.Words for .NET API 参考
description: DocSaveOptions 财产. 当错误的出于性能原因小图元文件不会被压缩 默认值为真的所有图元文件无论其大小如何都会被压缩
type: docs
weight: 20
url: /zh/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

当`错误的`，出于性能原因，小图元文件不会被压缩。 默认值为`真的`，所有图元文件无论其大小如何都会被压缩。

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

### 例子

演示如何在保存时更改文档中的图元文件压缩。

```csharp
// 打开包含 Microsoft Equation 3.0 公式的文档。
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// 当我们保存文档时，出于性能原因，较小的图元文件不会被压缩。
// 我们可以在 SaveOptions 对象中设置一个标志，以在保存时压缩每个图元文件。
// 某些编辑器（例如 LibreOffice）无法读取未压缩的图元文件。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);

if (compressAllMetafiles)
    Assert.That(10000, Is.LessThan(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
else
    Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx").Length));
```

### 也可以看看

* class [DocSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../docsaveoptions/)
* 部件 [Aspose.Words](../../../)


