---
title: XlsxSaveOptions.CompressionLevel
second_title: Aspose.Words for .NET API 参考
description: XlsxSaveOptions 财产. 指定用于保存文档的压缩级别 默认值为Normal.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

指定用于保存文档的压缩级别。 默认值为Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### 例子

演示如何压缩 XLSX 文档。

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum; 

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### 也可以看看

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../xlsxsaveoptions/)
* 部件 [Aspose.Words](../../../)


