---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words for .NET
description: 探索 FontInfoCollection 的 EmbedSystemFonts 属性如何通过嵌入系统字体来增强您的文档。了解其默认值和优势！
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

指定是否将系统字体嵌入到文档中。 此属性的默认值为`错误的`。

此选项仅在以下情况下有效[`EmbedTrueTypeFonts`](../embedtruetypefonts/)选项设置为`真的`。

```csharp
public bool EmbedSystemFonts { get; set; }
```

## 评论

将此属性设置为`真的`如果用户使用的是东亚系统，并且希望创建一个可供其他系统上没有该语言字体的用户阅读的文档，则此功能非常有用。例如，使用日语系统的用户可以选择在文档中嵌入日语字体，这样该日语文档在所有系统上都可以阅读。

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
