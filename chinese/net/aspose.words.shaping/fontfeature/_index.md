---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Shaping.FontFeature 枚举，详细了解字体中用于脚本渲染的字形用法。立即提升您的排版知识！
type: docs
weight: 6860
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
| GlyphCompositionDecomposition | `1667460464` | 为了最大限度地减少字形替代的数量，有时需要将字符的默认字形分解为两个或多个字形。 此外，为了更好地进行字形处理，最好将两个或多个字符的默认字形组合成一个字形。 此功能允许此类组合/分解。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp 等效 OpenType 标签：“ccmp” |
| StandardLigatures | `1818847073` | 将一系列字形替换为适合排版目的的单个字形。 此功能涵盖设计师/制造商判断在正常情况下应使用的连字。 等效 OpenType 标签：“liga” https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | 将一系列字形替换为适合排版目的的单个字形。 此功能涵盖脚本确定在正常情况下需要使用的连字。 此功能对于某些脚本很重要，可确保正确的字形形成。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig 等效 OpenType 标签：“rlig” |
| ContextualLigatures | `1668049255` | 将一系列字形替换为单个更适合排版用途的字形。 与其他连字功能不同，“clig”指定推荐使用连字的上下文。 此功能在某些脚本设计和花体连字中很重要。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig 等效 OpenType 标签：“clig” |
| DiscretionaryLigatures | `1684826471` | 将一系列字形替换为适合排版目的的单个字形。 此功能涵盖可根据用户喜好用于特殊效果的连字。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig 等效 OpenType 标签：“dlig” |
| HistoricalLigatures | `1751935335` | 一些连字在过去很常用，但今天看来却不合时宜。 一些字体包含历史形式作为替代形式，因此它们可用于产生“时期”效果。 此功能将默认（当前）形式替换为历史替代形式。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig 等效 OpenType 标签：“hlig” |
| ProportionalFigures | `1886287213` | 将以统一（表格）宽度设置的图形字形替换为以特定于字形（比例）的宽度设置的相应字形。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum 等效 OpenType 标签：'pnum' |
| TabularFigures | `1953396077` | 将按比例宽度设置的图形字形替换为按统一（表格）宽度设置的相应字形。 表格宽度通常是默认设置，但不能安全地假设这一点。 当然，此功能不会出现在等宽设计中。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum 等效 OpenType 标签：“tnum” |
| LiningFigures | `1819178349` | 此功能将选定的非衬线数字更改为衬线数字。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum 等效的 OpenType 标签：“lnum” |
| OldstyleFigures | `1869509997` | 此功能将选定的数字从默认或衬线样式更改为旧样式。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum 等效的 OpenType 标签：“onum” |
| VerticalAlternates | `1986359924` | 将默认字形转换为适合垂直书写模式下直立呈现的字形。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert 等效 OpenType 标签：“vert” |
| VerticalAlternatesAndRotation | `1987212338` | 将一些固定宽度（半宽、三分之一宽或四分之一宽）或比例宽度的字形（主要是拉丁字母或片假名） 替换为适合垂直书写的形式（即顺时针旋转 90 度）。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 等效的 OpenType 标签：“vrt2” |
| StylisticSet01 | `1936928817` | 风格集 1 除了或代替单个字形的风格替代（参见“盐”功能）之外， 某些字体可能包含与字符集部分相对应的风格变体字形集，例如拉丁字体中小写字母的多个变体。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 等效 OpenType 标签：'ss01' |
| StylisticSet02 | `1936928818` | 风格集 2 等效 OpenType 标签：'ss02' |
| StylisticSet03 | `1936928819` | 风格集 3 等效 OpenType 标签：'ss03' |
| StylisticSet04 | `1936928820` | 风格集 4 等效 OpenType 标签：'ss04' |
| StylisticSet05 | `1936928821` | 风格集 5 等效 OpenType 标签：'ss05' |
| StylisticSet06 | `1936928822` | 风格集 6 等效 OpenType 标签：'ss06' |
| StylisticSet07 | `1936928823` | 风格集 7 等效 OpenType 标签：'ss07' |
| StylisticSet08 | `1936928824` | 风格集 8 等效 OpenType 标签：'ss08' |
| StylisticSet09 | `1936928825` | 风格集 9 等效 OpenType 标签：'ss09' |
| StylisticSet10 | `1936929072` | 风格集 10 等效 OpenType 标签：'ss10' |
| StylisticSet11 | `1936929073` | 风格集 11 等效 OpenType 标签：'ss11' |
| StylisticSet12 | `1936929074` | 风格集 12 等效 OpenType 标签：'ss12' |
| StylisticSet13 | `1936929075` | 风格集 13 等效 OpenType 标签：'ss13' |
| StylisticSet14 | `1936929076` | 风格集 14 等效 OpenType 标签：'ss14' |
| StylisticSet15 | `1936929077` | 风格集 15 等效 OpenType 标签：'ss15' |
| StylisticSet16 | `1936929078` | 风格集 16 等效 OpenType 标签：'ss16' |
| StylisticSet17 | `1936929079` | 风格集 17 等效 OpenType 标签：'ss17' |
| StylisticSet18 | `1936929080` | 风格集 18 等效 OpenType 标签：'ss18' |
| StylisticSet19 | `1936929081` | 风格集 19 等效 OpenType 标签：'ss19' |
| StylisticSet20 | `1936929328` | 风格集 20 等效 OpenType 标签：'ss20' |
| Kerning | `1801810542` | 调整字形之间的空间量，通常是为了在字形之间提供视觉上一致的间距。 尽管设计精良的字体总体上具有一致的字形间距，但某些字形组合需要进行调整以提高可读性。 除了水平方向的标准调整外，此功能还可以通过设备表提供与大小相关的字距调整数据， Y 文本方向的“跨流”字距调整，以及独立于高级调整的字形位置调整。 请注意，此功能可能适用于两个以上字形的运行，并且不会在等宽字体中使用。 另请注意，此功能不适用于垂直设置的文本。 https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern 等效的 OpenType 标签： ‘kern’ |

### 也可以看看

* 命名空间 [Aspose.Words.Shaping](../../aspose.words.shaping/)
* 部件 [Aspose.Words](../../)
