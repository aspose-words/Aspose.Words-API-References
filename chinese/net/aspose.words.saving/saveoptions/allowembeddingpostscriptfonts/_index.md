---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words for .NET
description: 使用 SaveOptions 的 AllowEmbeddingPostScriptFonts 控制文档中的字体嵌入。轻松管理 TrueType 字体选项，提升文档质量。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

获取或设置一个布尔值，指示在保存文档时嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体 。 默认值为`错误的`.

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## 评论

请注意，Word 不嵌入 PostScript 字体，但可以打开嵌入此类字体的文档。

此选项仅在以下情况下有效[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/)the 的[`FontInfos`](../../../aspose.words/documentbase/fontinfos/)属性设置为`真的`。

## 例子

展示如何使用 PostScript 字体保存文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// 使用 PostScript 加载字体以在文档中使用。
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// 嵌入 TrueType 字体。
doc.FontInfos.EmbedTrueTypeFonts = true;

// 允许在嵌入 TrueType 字体的同时嵌入 PostScript 字体。
// Microsoft Word 不嵌入 PostScript 字体，但可以打开嵌入此类型字体的文档。
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### 也可以看看

* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
