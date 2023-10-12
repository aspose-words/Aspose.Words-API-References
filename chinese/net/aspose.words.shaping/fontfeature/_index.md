---
title: Enum FontFeature
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Shaping.FontFeature 枚举. 功能提供有关如何在字体中使用字形来呈现脚本的信息 https//docs.microsoft.com/enus/typography/opentype/spec/featuretags
type: docs
weight: 6030
url: /zh/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

功能提供有关如何在字体中使用字形来呈现脚本的信息。 https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | 为了最大限度地减少替代字形的数量，有时需要将一个字符的默认字形分解为两个或多个字形。 此外，最好将两个或多个字符的默认字形组成一个字形以获得更好的字形处理。 此功能允许此类组合/分解。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp 等效 OpenType 标记：'ccmp' |
| StandardLigatures | `1818847073` | 用单个字形替换字形序列，这是印刷目的的首选。 此功能涵盖了设计者/制造商判断应在正常情况下使用的连字。 等效 OpenType 标记：'liga' https://docs .microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | 用单个字形替换字形序列，这对于印刷目的来说是首选。 此功能涵盖脚本确定在正常条件下使用所需的那些连字。 此功能对于某些脚本非常重要，可确保正确的字形形成. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig 等效 OpenType 标记：'rlig' |
| ContextualLigatures | `1668049255` | 用单个字形替换字形序列，这对于印刷目的来说是首选。 与其他连字功能不同，“clig”指定建议连字的上下文。 此功能在某些脚本设计和花体连字中非常重要。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig 等效 OpenType 标记：'clig' |
| DiscretionaryLigatures | `1684826471` | 将一系列字形替换为印刷目的首选的单个字形。 此功能涵盖了那些可根据用户的喜好用于特殊效果的连字。 https://docs.microsoft.com/en-us /typography/opentype/spec/features_ae#dlig 等效 OpenType 标记：'dlig' |
| HistoricalLigatures | `1751935335` | 一些连字在过去很常用，但今天显得不合时宜。 某些字体包括历史形式作为替代形式，因此它们可以用于“句点”效果。 此功能将默认（当前）形式替换为历史替代品。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig 等效 OpenType 标记：'hlig' |
| ProportionalFigures | `1886287213` | 将统一（表格）宽度上设置的图形字形替换为特定字形（比例）宽度上设置的相应字形。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum 等效 OpenType 标签：'pnum' |
| TabularFigures | `1953396077` | 将按比例宽度设置的图形字形替换为在统一（表格）宽度上设置的相应字形。 表格宽度通常是默认值，但这不能安全地假设。 当然，此功能不会出现在等宽设计中。 https ://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum 等效 OpenType 标记：'tnum' |
| LiningFigures | `1819178349` | 此功能将选定的非衬线数字更改为衬线数字。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum 等效 OpenType 标记：'lnum' |
| OldstyleFigures | `1869509997` | 此功能将选定的图形从默认或衬里样式更改为旧式形式。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum 等效 OpenType 标记：'onum' |
| VerticalAlternates | `1986359924` | 将默认字形转换为适合在垂直书写模式下直立呈现的字形。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert 等效 OpenType 标记：'vert' |
| VerticalAlternatesAndRotation | `1987212338` | 用适合垂直书写（即顺时针旋转 90 度）的形式替换一些固定宽度（半角、三分之一角或四分之一角）或比例宽度字形（主要是拉丁文或片假名） 。 https:// docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 等效 OpenType 标记：'vrt2' |
| StylisticSet01 | `1936928817` | 文体集 1 除了单个字形的文体替代方案（参见“盐”功能）之外， 某些字体可能包含与字符集部分相对应的文体变体字形集，例如，小写字母的多个变体拉丁字体。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 等效 OpenType 标记：'ss01' |
| StylisticSet02 | `1936928818` | 风格集 2 等效 OpenType 标记：'ss02' |
| StylisticSet03 | `1936928819` | 风格集 3 等效 OpenType 标签：'ss03' |
| StylisticSet04 | `1936928820` | 风格集 4 等效 OpenType 标签：'ss04' |
| StylisticSet05 | `1936928821` | 风格集 5 等效 OpenType 标签：'ss05' |
| StylisticSet06 | `1936928822` | 风格集 6 等效 OpenType 标签：'ss06' |
| StylisticSet07 | `1936928823` | 风格集 7 等效 OpenType 标签：'ss07' |
| StylisticSet08 | `1936928824` | 风格集 8 等效 OpenType 标记：'ss08' |
| StylisticSet09 | `1936928825` | 风格集 9 等效 OpenType 标签：'ss09' |
| StylisticSet10 | `1936929072` | 风格集 10 等效 OpenType 标记：'ss10' |
| StylisticSet11 | `1936929073` | 风格集 11 等效 OpenType 标记：'ss11' |
| StylisticSet12 | `1936929074` | 风格集 12 等效 OpenType 标记：'ss12' |
| StylisticSet13 | `1936929075` | 风格集 13 等效 OpenType 标记：'ss13' |
| StylisticSet14 | `1936929076` | 风格集 14 等效 OpenType 标签：'ss14' |
| StylisticSet15 | `1936929077` | 风格集 15 等效 OpenType 标签：'ss15' |
| StylisticSet16 | `1936929078` | 风格集 16 等效 OpenType 标记：'ss16' |
| StylisticSet17 | `1936929079` | 风格集 17 等效 OpenType 标签：'ss17' |
| StylisticSet18 | `1936929080` | 风格集 18 等效 OpenType 标签：'ss18' |
| StylisticSet19 | `1936929081` | 风格集 19 等效 OpenType 标签：'ss19' |
| StylisticSet20 | `1936929328` | 风格集 20 等效 OpenType 标签：'ss20' |
| Kerning | `1801810542` | 调整字形之间的间距量，通常是为了在字形之间提供视觉上一致的间距。 虽然精心设计的字体总体上具有一致的字形间距，但某些字形组合需要调整以提高易读性。 除了水平方向的标准调整之外，此功能可以通过设备表提供与大小相关的字距调整数据， Y 文本方向上的“跨流”字距调整，以及独立于高级调整的字形位置调整。 请注意，此功能可能适用于两个以上的运行字形，并且不会在等宽字体中使用。 另请注意，此功能不适用于垂直设置的文本。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern 等效OpenType 标签：'kern' |

### 也可以看看

* 命名空间 [Aspose.Words.Shaping](../../aspose.words.shaping/)
* 部件 [Aspose.Words](../../)


