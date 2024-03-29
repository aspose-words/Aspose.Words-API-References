---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: 用于 .NET 的 Aspose.Words
description: FontInfoCollection Item 财产. 获取具有指定名称的字体 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/fontinfocollection/item/
---
## FontInfoCollection indexer (1 of 2)

获取具有指定名称的字体。

```csharp
public FontInfo this[string name] { get; }
```

| 范围 | 描述 |
| --- | --- |
| name | 要查找的字体名称，不区分大小写。 |

## 例子

演示如何从文档中提取嵌入字体，并将其保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入的字体格式可能与其他格式（例如.doc）不同。
// 在提取字体之前，我们需要知道正确的格式。
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// 此外，我们还可以将来自 .doc 文档的嵌入式 OpenType 格式转换为 OpenType。
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### 也可以看看

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)

---

## FontInfoCollection indexer (2 of 2)

获取指定索引处的字体。

```csharp
public FontInfo this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 字体的从零开始的索引。 |

## 例子

演示如何从文档中提取嵌入字体，并将其保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入的字体格式可能与其他格式（例如.doc）不同。
// 在提取字体之前，我们需要知道正确的格式。
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// 此外，我们还可以将来自 .doc 文档的嵌入式 OpenType 格式转换为 OpenType。
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### 也可以看看

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
