---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: 发现 XlsxSaveOptions CompressionLevel 属性，通过可自定义的压缩设置优化文档保存，实现高效的文件管理。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

指定用于保存文档的压缩级别。 默认值为Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## 例子

展示如何压缩 XLSX 文档。

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### 也可以看看

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
