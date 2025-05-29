---
title: EmbeddedFontFormat Enum
linktitle: EmbeddedFontFormat
articleTitle: EmbeddedFontFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.EmbeddedFontFormat 枚举，它定义了 FontInfo 对象中嵌入字体的格式，以增强文档样式。
type: docs
weight: 3260
url: /zh/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

指定内部嵌入特定字体的格式[`FontInfo`](../fontinfo/)目的。

将文档保存为文件时，仅记录相应格式的嵌入字体。

```csharp
public enum EmbeddedFontFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmbeddedOpenType | `0` | 指定嵌入式 OpenType (EOT) 文件格式。 |
| OpenType | `1` | 指定字体，嵌入为 OpenType（TrueType）字体文件的普通副本。 |

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

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
