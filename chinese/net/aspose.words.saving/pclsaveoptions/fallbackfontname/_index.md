---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: 用于 .NET 的 Aspose.Words
description: PclSaveOptions FallbackFontName 财产. 如果在打印机和内置字体集合中找不到所需字体则将使用 的字体名称 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

如果在打印机和内置字体集合中找不到所需字体，则将使用 的字体名称。

```csharp
public string FallbackFontName { get; set; }
```

## 评论

如果未找到后备，则会生成警告并使用“Arial”字体。

## 例子

演示如何声明打印机将应用于打印文本的字体，作为原始字体不可用时的替代字体。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// 此文档将指示打印机将“Times New Roman”应用到缺少字体的文本。
// 如果“Times New Roman”也不可用，打印机将默认使用“Arial”字体。
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### 也可以看看

* class [PclSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
