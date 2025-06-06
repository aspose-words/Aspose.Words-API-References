---
title: FontInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 发现 FontInfoCollection Item 属性，轻松地按名称检索字体，以精确度和风格增强您的设计项目。
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
| name | 要定位的字体的不区分大小写的名称。 |

## 例子

展示如何从文档中提取嵌入字体并将其保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入字体格式在其他格式（如 .doc）中可能有所不同。
// 我们需要知道正确的格式才能提取字体。
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// 另外，我们可以将来自 .doc 文档的嵌入式 OpenType 格式转换为 OpenType。
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

展示如何从文档中提取嵌入字体并将其保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入字体格式在其他格式（如 .doc）中可能有所不同。
// 我们需要知道正确的格式才能提取字体。
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// 另外，我们可以将来自 .doc 文档的嵌入式 OpenType 格式转换为 OpenType。
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### 也可以看看

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
