---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontInfo 类，这是您了解文档详细字体的关键，可提高文本质量和视觉吸引力。
type: docs
weight: 3350
url: /zh/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

指定有关文档中使用的字体的信息。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class FontInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | 获取或设置字体的替代名称。 |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | 获取或设置字体的字符集。 |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | 获取嵌入字体许可权。 |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | 获取或设置此字体所属的字体系列。 |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | 表示此字体是 TrueType 或 OpenType 字体，而不是光栅字体或矢量字体。 默认值为`真的`. |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | 获取字体的名称。 |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | 获取或设置 PANOSE 字体分类编号。 |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | 间距指示字体是否为固定间距、按比例间隔或依赖于默认设置。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | 获取特定的嵌入字体文件。 |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | 获取 OpenType 格式的嵌入字体文件。嵌入 OpenType 格式的字体将转换为 OpenType 格式。 |

## 评论

您不能直接创建此类的实例。 使用[`FontInfos`](../../aspose.words/documentbase/fontinfos/)属性来访问文档中定义的 fonts 集合。

## 例子

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

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
