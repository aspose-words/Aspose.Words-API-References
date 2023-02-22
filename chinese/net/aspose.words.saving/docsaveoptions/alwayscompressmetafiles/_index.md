---
title: DocSaveOptions.AlwaysCompressMetafiles
second_title: Aspose.Words for .NET API 参考
description: DocSaveOptions 财产. 什么时候错误的 出于性能原因不会压缩小元文件 默认值为 真的所有元文件都被压缩无论其大小
type: docs
weight: 20
url: /zh/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

什么时候`错误的` 出于性能原因，不会压缩小元文件。 默认值为 **真的**，所有元文件都被压缩，无论其大小。

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

### 例子

显示如何在保存时更改文档中的元文件压缩。

```csharp
// 打开一个包含 Microsoft Equation 3.0 公式的文档。
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// 当我们保存文档时，出于性能原因，不会压缩较小的元文件。
// 我们可以在 SaveOptions 对象中设置一个标志，以便在保存时压缩每个图元文件。
// LibreOffice 等一些编辑器无法读取未压缩的元文件。
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


