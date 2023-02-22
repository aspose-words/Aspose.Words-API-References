---
title: Enum EmbeddedFontFormat
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.EmbeddedFontFormat 枚举. 指定内部特定嵌入字体的格式FontInfo目的
type: docs
weight: 2670
url: /zh/net/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enumeration

指定内部特定嵌入字体的格式[`FontInfo`](../fontinfo/)目的。

将文档保存到文件时，只记下相应格式的嵌入字体。

```csharp
public enum EmbeddedFontFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmbeddedOpenType | `0` | 指定嵌入式 OpenType (EOT) 文件格式。 |
| OpenType | `1` | 指定字体，嵌入为 OpenType (TrueType) 字体文件的纯副本。 |

### 例子

演示如何从文档中提取嵌入字体，并将其保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// 嵌入的字体格式可能与.doc等其他格式不同。
// 在提取字体之前，我们需要知道正确的格式。
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// 此外，我们可以将来自 .doc 文档的嵌入式 OpenType 格式转换为 OpenType。
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)


