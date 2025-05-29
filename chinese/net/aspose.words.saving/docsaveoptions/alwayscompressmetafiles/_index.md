---
title: DocSaveOptions.AlwaysCompressMetafiles
linktitle: AlwaysCompressMetafiles
articleTitle: AlwaysCompressMetafiles
second_title: Aspose.Words for .NET
description: 使用 AlwaysCompressMetafiles 属性优化文档管理。通过控制图元文件压缩来提高效率，从而提升性能。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/docsaveoptions/alwayscompressmetafiles/
---
## DocSaveOptions.AlwaysCompressMetafiles property

当`错误的`，出于性能原因，小型元文件不会被压缩。 默认值为`真的`，所有图元文件无论大小都会被压缩。

```csharp
public bool AlwaysCompressMetafiles { get; set; }
```

## 例子

展示如何在保存时更改文档中的元文件压缩。

```csharp
// 打开包含 Microsoft Equation 3.0 公式的文档。
Document doc = new Document(MyDir + "Microsoft equation object.docx");

// 当我们保存文档时，出于性能原因，较小的元文件不会被压缩。
// 我们可以在 SaveOptions 对象中设置一个标志，以便在保存时压缩每个元文件。
// 某些编辑器（例如 LibreOffice）无法读取未压缩的元文件。
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.AlwaysCompressMetafiles = compressAllMetafiles;

doc.Save(ArtifactsDir + "DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

### 也可以看看

* class [DocSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
