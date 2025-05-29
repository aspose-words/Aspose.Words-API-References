---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words for .NET
description: 使用 DocumentBase 的 FontInfos 功能访问详细的字体属性，轻松增强文档的设计和可读性。
type: docs
weight: 30
url: /zh/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

提供对本文档中使用的字体属性的访问。

```csharp
public FontInfoCollection FontInfos { get; }
```

## 评论

此字体定义集合按原样从文档中加载。 字体定义在某些文档中可能是可选的、缺失的或不完整的。

不要依赖此集合来确定文档中使用了特定字体。 您应该只使用此集合来获取有关文档中可能使用的字体的信息。

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

显示如何打印文档中存在的字体的详细信息。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// 打印文档中所有已使用和未使用的字体。
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### 也可以看看

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
