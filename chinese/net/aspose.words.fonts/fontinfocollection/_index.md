---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontInfoCollection 类，这是您有效管理文档字体和增强文档视觉吸引力的首选解决方案。
type: docs
weight: 3360
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
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | 指定是否将系统字体嵌入到文档中。 此属性的默认值为`错误的`。 |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | 指定在保存文档时是否嵌入 TrueType 字体。 此属性的默认值为`错误的`. |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | 获取具有指定名称的字体。 (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | 指定是否将嵌入的 TrueType 字体子集与文档一起保存。 此属性的默认值为`错误的`。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | 确定集合是否包含具有给定名称的字体。 |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |

## 评论

项目是[`FontInfo`](../fontinfo/)对象。

您不能直接创建此类的实例。 使用[`FontInfos`](../../aspose.words/documentbase/fontinfos/)属性来访问文档中定义的字体集合 。

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

* class [FontInfo](../fontinfo/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
