---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: 用于 .NET 的 Aspose.Words
description: FontInfoCollection EmbedTrueTypeFonts 财产. 指定保存文档时是否在文档中嵌入 TrueType 字体 此属性的默认值为错误的 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

指定保存文档时是否在文档中嵌入 TrueType 字体。 此属性的默认值为`错误的`.

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## 评论

嵌入 TrueType 字体允许其他人使用用于创建文档的相同字体查看文档， ，但可能会大大增加文档大小。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

## 例子

演示如何保存嵌入 TrueType 字体的文档。

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### 也可以看看

* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
