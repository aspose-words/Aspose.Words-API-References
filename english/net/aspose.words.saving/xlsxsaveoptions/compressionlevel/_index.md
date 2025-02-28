---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: Discover the XlsxSaveOptions CompressionLevel property to optimize document saving with customizable compression settings for efficient file management.
type: docs
weight: 20
url: /net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Specifies the compression level used to save document. The default value is Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Examples

Shows how to compress XLSX document.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### See Also

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
