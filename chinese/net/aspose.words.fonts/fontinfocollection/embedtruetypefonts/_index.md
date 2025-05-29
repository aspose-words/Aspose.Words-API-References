---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words for .NET
description: 了解 FontInfoCollection 中的 EmbedTrueTypeFonts 属性如何通过允许嵌入 TrueType 字体来提升文档质量。默认值为 false。
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

指定在保存文档时是否嵌入 TrueType 字体。 此属性的默认值为`错误的`.

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## 评论

嵌入 TrueType 字体可让其他人使用创建文档时所用的相同字体来查看文档， 但可能会大大增加文档的大小。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

## 例子

展示如何保存嵌入 TrueType 字体的文档。

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### 也可以看看

* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
