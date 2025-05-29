---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words for .NET
description: 发现 PclSaveOptions FallbackFontName 属性，确保在所需字体不可用时使用默认字体进行无缝打印。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

如果在打印机和内置字体集合中未找到所需字体，则将使用的字体名称。

```csharp
public string FallbackFontName { get; set; }
```

## 评论

如果没有找到后备字体，则会生成警告并使用“Arial”字体。

## 例子

说明如何声明一种字体，当原始字体不可用时，打印机将使用该字体来替代打印的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// 本文档将指示打印机将“Times New Roman”应用于缺少字体的文本。
// 如果“Times New Roman”也不可用，打印机将默认使用“Arial”字体。
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### 也可以看看

* class [PclSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
