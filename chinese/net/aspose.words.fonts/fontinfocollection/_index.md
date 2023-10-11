---
title: Class FontInfoCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.FontInfoCollection 班级. 表示文档中使用的字体集合
type: docs
weight: 2930
url: /zh/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

表示文档中使用的字体集合。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | 指定是否将系统字体嵌入到文档中。 该属性的默认值为`错误的`。 |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | 指定保存文档时是否在文档中嵌入 TrueType 字体。 此属性的默认值为`错误的`. |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | 获取具有指定名称的字体。 (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | 指定是否将嵌入的 TrueType 字体的子集与文档一起保存。 此属性的默认值为`错误的`。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(string) | 确定集合中是否包含具有给定名称的字体。 |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |

### 评论

物品有[`FontInfo`](../fontinfo/)对象。

您不直接创建此类的实例。 使用[`FontInfos`](../../aspose.words/documentbase/fontinfos/)属性来访问文档中定义的字体 集合。

### 例子

演示如何打印文档中存在的字体的详细信息。

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

* class [FontInfo](../fontinfo/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)


