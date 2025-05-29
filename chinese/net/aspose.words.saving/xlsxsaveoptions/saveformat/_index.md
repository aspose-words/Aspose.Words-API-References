---
title: XlsxSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 发现 XlsxSaveOptions SaveFormat 属性，轻松地以 Xlsx 格式保存文档，确保文件的兼容性和质量。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/xlsxsaveoptions/saveformat/
---
## XlsxSaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是Xlsx.

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XlsxSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
