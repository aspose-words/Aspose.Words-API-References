---
title: FontInfoCollection.SaveSubsetFonts
second_title: Aspose.Words for .NET API 参考
description: FontInfoCollection 财产. 指定是否将嵌入的 TrueType 字体的子集与文档一起保存 此属性的默认值为错误的
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

指定是否将嵌入的 TrueType 字体的子集与文档一起保存。 此属性的默认值为`错误的`。

此选项仅在以下情况下有效[`EmbedTrueTypeFonts`](../embedtruetypefonts/)属性设置为`真的`。

```csharp
public bool SaveSubsetFonts { get; set; }
```

### 评论

此选项仅适用于 DOC、DOCX 和 RTF 格式。

### 例子

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
* 命名空间 [Aspose.Words.Fonts](../../fontinfocollection/)
* 部件 [Aspose.Words](../../../)


