---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.FontInfo 班级. 指定文档中使用的字体信息 在 C#.
type: docs
weight: 2920
url: /zh/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

指定文档中使用的字体信息。

```csharp
public class FontInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | 获取或设置字体的备用名称。 |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | 获取或设置字体的字符集。 |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | 获取或设置该字体所属的字体系列。 |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | 表示此字体是 TrueType 或 OpenType 字体，而不是光栅或矢量字体。 默认为 true。 |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | 获取字体名称。 |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | 获取或设置 PANOSE 字体分类号。 |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | 间距指示字体是固定间距、按比例间隔还是依赖于默认设置。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | 获取特定的嵌入字体文件。 |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | 获取 OpenType 格式的嵌入字体文件。 Embedded OpenType 格式的字体转换为 OpenType. |

## 评论

您不直接创建此类的实例。 使用[`FontInfos`](../../aspose.words/documentbase/fontinfos/)属性来访问文档中定义的字体集合 。

## 例子

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

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
