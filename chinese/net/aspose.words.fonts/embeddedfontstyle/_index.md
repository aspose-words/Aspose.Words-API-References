---
title: EmbeddedFontStyle Enum
linktitle: EmbeddedFontStyle
articleTitle: EmbeddedFontStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words EmbeddedFontStyle 枚举，轻松管理 FontInfo 对象中嵌入的字体样式，增强文档格式化功能。
type: docs
weight: 3270
url: /zh/net/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enumeration

指定嵌入字体的样式[`FontInfo`](../fontinfo/)对象.

```csharp
[Flags]
public enum EmbeddedFontStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Regular | `0` | 指定常规嵌入字体。 |
| Bold | `1` | 指定粗体嵌入字体。 |
| Italic | `2` | 指定斜体嵌入字体。 |
| BoldItalic | `3` | 指定粗体斜体嵌入字体。 |

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
