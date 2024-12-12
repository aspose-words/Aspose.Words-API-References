---
title: FontFeature enumeration
linktitle: FontFeature enumeration
articleTitle: FontFeature enumeration
second_title: Aspose.Words for Python
description: "aspose.words.shaping.FontFeature enumeration. Features provide information about how glyphs are used in a font to render a script"
type: docs
weight: 40
url: /python-net/aspose.words.shaping/fontfeature/
---

## FontFeature enumeration

Features provide information about how glyphs are used in a font to render a script.
https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags


### Members

| Name | Description |
| --- | --- |
| GLYPH_COMPOSITION_DECOMPOSITION | To minimize the number of glyph alternates, it is sometimes desirable to decompose the default glyph for a character into two or more glyphs. Additionally, it may be preferable to compose default glyphs for two or more characters into a single glyph for better glyph processing. This feature permits such composition/decomposition. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Equivalent OpenType tag: 'ccmp' |
| STANDARD_LIGATURES | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers the ligatures which the designer/manufacturer judges should be used in normal conditions. Equivalent OpenType tag: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| REQUIRED_LIGATURES | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers those ligatures, which the script determines as required to be used in normal conditions. This feature is important for some scripts to ensure correct glyph formation. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Equivalent OpenType tag: 'rlig' |
| CONTEXTUAL_LIGATURES | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. Unlike other ligature features, 'clig' specifies the context in which the ligature is recommended. This capability is important in some script designs and for swash ligatures. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Equivalent OpenType tag: 'clig' |
| DISCRETIONARY_LIGATURES | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers those ligatures which may be used for special effect, at the user’s preference. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Equivalent OpenType tag: 'dlig' |
| HISTORICAL_LIGATURES | Some ligatures were in common use in the past, but appear anachronistic today. Some fonts include the historical forms as alternates, so they can be used for a "period" effect. This feature replaces the default (current) forms with the historical alternates. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Equivalent OpenType tag: 'hlig' |
| PROPORTIONAL_FIGURES | Replaces figure glyphs set on uniform (tabular) widths with corresponding glyphs set on glyph-specific (proportional) widths. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Equivalent OpenType tag: 'pnum' |
| TABULAR_FIGURES | Replaces figure glyphs set on proportional widths with corresponding glyphs set on uniform (tabular) widths. Tabular widths will generally be the default, but this cannot be safely assumed. Of course this feature would not be present in monospaced designs. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Equivalent OpenType tag: 'tnum' |
| LINING_FIGURES | This feature changes selected non-lining figures to lining figures. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Equivalent OpenType tag: 'lnum' |
| OLDSTYLE_FIGURES | This feature changes selected figures from the default or lining style to oldstyle form. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Equivalent OpenType tag: 'onum' |
| VERTICAL_ALTERNATES | Transforms default glyphs into glyphs that are appropriate for upright presentation in vertical writing mode. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Equivalent OpenType tag: 'vert' |
| VERTICAL_ALTERNATES_AND_ROTATION | Replaces some fixed-width (half-, third- or quarter-width) or proportional-width glyphs (mostly Latin or katakana) with forms suitable for vertical writing (that is, rotated 90 degrees clockwise). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Equivalent OpenType tag: 'vrt2' |
| STYLISTIC_SET01 | Stylistic Set 1 In addition to, or instead of, stylistic alternatives of individual glyphs (see 'salt' feature), some fonts may contain sets of stylistic variant glyphs corresponding to portions of the character set, e.g. multiple variants for lowercase letters in a Latin font. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Equivalent OpenType tag: 'ss01' |
| STYLISTIC_SET02 | Stylistic Set 2 Equivalent OpenType tag: 'ss02' |
| STYLISTIC_SET03 | Stylistic Set 3 Equivalent OpenType tag: 'ss03' |
| STYLISTIC_SET04 | Stylistic Set 4 Equivalent OpenType tag: 'ss04' |
| STYLISTIC_SET05 | Stylistic Set 5 Equivalent OpenType tag: 'ss05' |
| STYLISTIC_SET06 | Stylistic Set 6 Equivalent OpenType tag: 'ss06' |
| STYLISTIC_SET07 | Stylistic Set 7 Equivalent OpenType tag: 'ss07' |
| STYLISTIC_SET08 | Stylistic Set 8 Equivalent OpenType tag: 'ss08' |
| STYLISTIC_SET09 | Stylistic Set 9 Equivalent OpenType tag: 'ss09' |
| STYLISTIC_SET10 | Stylistic Set 10 Equivalent OpenType tag: 'ss10' |
| STYLISTIC_SET11 | Stylistic Set 11 Equivalent OpenType tag: 'ss11' |
| STYLISTIC_SET12 | Stylistic Set 12 Equivalent OpenType tag: 'ss12' |
| STYLISTIC_SET13 | Stylistic Set 13 Equivalent OpenType tag: 'ss13' |
| STYLISTIC_SET14 | Stylistic Set 14 Equivalent OpenType tag: 'ss14' |
| STYLISTIC_SET15 | Stylistic Set 15 Equivalent OpenType tag: 'ss15' |
| STYLISTIC_SET16 | Stylistic Set 16 Equivalent OpenType tag: 'ss16' |
| STYLISTIC_SET17 | Stylistic Set 17 Equivalent OpenType tag: 'ss17' |
| STYLISTIC_SET18 | Stylistic Set 18 Equivalent OpenType tag: 'ss18' |
| STYLISTIC_SET19 | Stylistic Set 19 Equivalent OpenType tag: 'ss19' |
| STYLISTIC_SET20 | Stylistic Set 20 Equivalent OpenType tag: 'ss20' |
| KERNING | Adjusts amount of space between glyphs, generally to provide optically consistent spacing between glyphs. Although a well-designed typeface has consistent inter-glyph spacing overall, some glyph combinations require adjustment for improved legibility. Besides standard adjustment in the horizontal direction, this feature can supply size-dependent kerning data via device tables, "cross-stream" kerning in the Y text direction, and adjustment of glyph placement independent of the advance adjustment. Note that this feature may apply to runs of more than two glyphs, and would not be used in monospaced fonts. Also note that this feature does not apply to text set vertically. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Equivalent OpenType tag: 'kern' |

### See Also

* module [aspose.words.shaping](../)

