---
title: DocumentBase.FontInfos
second_title: Aspose.Words for .NET API 参考
description: DocumentBase 财产. 提供对本文档中使用的字体属性的访问
type: docs
weight: 30
url: /zh/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

提供对本文档中使用的字体属性的访问。

```csharp
public FontInfoCollection FontInfos { get; }
```

### 评论

此字体定义集合按原样从文档中加载。 在某些文档中，字体定义可能是可选的、缺失的或不完整的。

不要依赖此集合来确定文档中是否使用了特定字体。 您应该只使用此集合来获取有关文档中可能使用的字体的信息。

### 例子

显示如何打印文档中存在的字体的详细信息。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// 打印文档中所有使用和未使用的字体。
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

显示如何使用嵌入的 TrueType 字体保存文档。

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)


