---
title: FontFeature
linktitle: FontFeature
second_title: Aspose.Words for Java
description: Features provide information about how glyphs are used in a font to render a script in Java.
type: docs
weight: 322
url: /java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Features provide information about how glyphs are used in a font to render a script. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Fields

| Field | Description |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | To minimize the number of glyph alternates, it is sometimes desirable to decompose the default glyph for a character into two or more glyphs. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Some ligatures were in common use in the past, but appear anachronistic today. |
| [KERNING](#KERNING) | Adjusts amount of space between glyphs, generally to provide optically consistent spacing between glyphs. |
| [LINING_FIGURES](#LINING-FIGURES) | This feature changes selected non-lining figures to lining figures. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | This feature changes selected figures from the default or lining style to oldstyle form. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Replaces figure glyphs set on uniform (tabular) widths with corresponding glyphs set on glyph-specific (proportional) widths. |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Stylistic Set 1 In addition to, or instead of, stylistic alternatives of individual glyphs (see 'salt' feature), some fonts may contain sets of stylistic variant glyphs corresponding to portions of the character set, e.g. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Stylistic Set 2 Equivalent OpenType tag: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Stylistic Set 3 Equivalent OpenType tag: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Stylistic Set 4 Equivalent OpenType tag: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Stylistic Set 5 Equivalent OpenType tag: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Stylistic Set 6 Equivalent OpenType tag: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Stylistic Set 7 Equivalent OpenType tag: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Stylistic Set 8 Equivalent OpenType tag: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Stylistic Set 9 Equivalent OpenType tag: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Stylistic Set 10 Equivalent OpenType tag: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Stylistic Set 11 Equivalent OpenType tag: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Stylistic Set 12 Equivalent OpenType tag: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Stylistic Set 13 Equivalent OpenType tag: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Stylistic Set 14 Equivalent OpenType tag: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Stylistic Set 15 Equivalent OpenType tag: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Stylistic Set 16 Equivalent OpenType tag: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Stylistic Set 17 Equivalent OpenType tag: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Stylistic Set 18 Equivalent OpenType tag: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Stylistic Set 19 Equivalent OpenType tag: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Stylistic Set 20 Equivalent OpenType tag: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Replaces figure glyphs set on proportional widths with corresponding glyphs set on uniform (tabular) widths. |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Transforms default glyphs into glyphs that are appropriate for upright presentation in vertical writing mode. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Replaces some fixed-width (half-, third- or quarter-width) or proportional-width glyphs (mostly Latin or katakana) with forms suitable for vertical writing (that is, rotated 90 degrees clockwise). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. Unlike other ligature features, 'clig' specifies the context in which the ligature is recommended. This capability is important in some script designs and for swash ligatures. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Equivalent OpenType tag: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers those ligatures which may be used for special effect, at the user\\u2019s preference. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Equivalent OpenType tag: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


To minimize the number of glyph alternates, it is sometimes desirable to decompose the default glyph for a character into two or more glyphs. Additionally, it may be preferable to compose default glyphs for two or more characters into a single glyph for better glyph processing. This feature permits such composition/decomposition. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp Equivalent OpenType tag: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Some ligatures were in common use in the past, but appear anachronistic today. Some fonts include the historical forms as alternates, so they can be used for a "period" effect. This feature replaces the default (current) forms with the historical alternates. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig Equivalent OpenType tag: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Adjusts amount of space between glyphs, generally to provide optically consistent spacing between glyphs. Although a well-designed typeface has consistent inter-glyph spacing overall, some glyph combinations require adjustment for improved legibility. Besides standard adjustment in the horizontal direction, this feature can supply size-dependent kerning data via device tables, "cross-stream" kerning in the Y text direction, and adjustment of glyph placement independent of the advance adjustment. Note that this feature may apply to runs of more than two glyphs, and would not be used in monospaced fonts. Also note that this feature does not apply to text set vertically. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern Equivalent OpenType tag: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


This feature changes selected non-lining figures to lining figures. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum Equivalent OpenType tag: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


This feature changes selected figures from the default or lining style to oldstyle form. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum Equivalent OpenType tag: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Replaces figure glyphs set on uniform (tabular) widths with corresponding glyphs set on glyph-specific (proportional) widths. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum Equivalent OpenType tag: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers those ligatures, which the script determines as required to be used in normal conditions. This feature is important for some scripts to ensure correct glyph formation. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig Equivalent OpenType tag: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Replaces a sequence of glyphs with a single glyph which is preferred for typographic purposes. This feature covers the ligatures which the designer/manufacturer judges should be used in normal conditions. Equivalent OpenType tag: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Stylistic Set 1 In addition to, or instead of, stylistic alternatives of individual glyphs (see 'salt' feature), some fonts may contain sets of stylistic variant glyphs corresponding to portions of the character set, e.g. multiple variants for lowercase letters in a Latin font. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 Equivalent OpenType tag: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Stylistic Set 2 Equivalent OpenType tag: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Stylistic Set 3 Equivalent OpenType tag: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Stylistic Set 4 Equivalent OpenType tag: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Stylistic Set 5 Equivalent OpenType tag: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Stylistic Set 6 Equivalent OpenType tag: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Stylistic Set 7 Equivalent OpenType tag: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Stylistic Set 8 Equivalent OpenType tag: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Stylistic Set 9 Equivalent OpenType tag: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Stylistic Set 10 Equivalent OpenType tag: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Stylistic Set 11 Equivalent OpenType tag: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Stylistic Set 12 Equivalent OpenType tag: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Stylistic Set 13 Equivalent OpenType tag: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Stylistic Set 14 Equivalent OpenType tag: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Stylistic Set 15 Equivalent OpenType tag: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Stylistic Set 16 Equivalent OpenType tag: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Stylistic Set 17 Equivalent OpenType tag: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Stylistic Set 18 Equivalent OpenType tag: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Stylistic Set 19 Equivalent OpenType tag: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Stylistic Set 20 Equivalent OpenType tag: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Replaces figure glyphs set on proportional widths with corresponding glyphs set on uniform (tabular) widths. Tabular widths will generally be the default, but this cannot be safely assumed. Of course this feature would not be present in monospaced designs. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum Equivalent OpenType tag: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Transforms default glyphs into glyphs that are appropriate for upright presentation in vertical writing mode. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert Equivalent OpenType tag: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Replaces some fixed-width (half-, third- or quarter-width) or proportional-width glyphs (mostly Latin or katakana) with forms suitable for vertical writing (that is, rotated 90 degrees clockwise). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 Equivalent OpenType tag: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFeature) {#toString-int}
```
public static String toString(int fontFeature)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
