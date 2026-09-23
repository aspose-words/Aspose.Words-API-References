---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words für Java"
description: "Features liefern Informationen darüber, wie Glyphen in einer Schrift verwendet werden, um ein Skript in Java darzustellen."
type: docs
weight: 325
url: /de/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Features liefern Informationen darüber, wie Glyphen in einer Schrift verwendet werden, um ein Skript darzustellen. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | Um die Anzahl der Glyphenalternativen zu minimieren, ist es manchmal wünschenswert, das Standardglyph für ein Zeichen in zwei oder mehr Glyphen zu zerlegen. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Einige Ligaturen waren früher gebräuchlich, wirken heute jedoch anachronistisch. |
| [KERNING](#KERNING) | Passt den Abstand zwischen Glyphen an, um im Allgemeinen optisch konsistente Abstände zwischen Glyphen zu gewährleisten. |
| [LINING_FIGURES](#LINING-FIGURES) | Dieses Feature ändert ausgewählte nicht‑linierende Ziffern in linierende Ziffern. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | Dieses Feature ändert ausgewählte Ziffern vom Standard‑ oder Linierstil in die Altstil‑Form. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Ersetzt Ziffernglyphen, die auf einheitlichen (tabellarischen) Breiten gesetzt sind, durch entsprechende Glyphen, die auf glyph‑spezifischen (proportionalen) Breiten gesetzt sind. |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Stilistisches Set 1 Zusätzlich zu oder anstelle von stilistischen Alternativen einzelner Glyphen (siehe 'salt'-Funktion), können einige Schriftarten Sets von stilistischen Varianten‑Glyphen enthalten, die entsprechenden Teilen des Zeichensatzes entsprechen, z. B. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Stilistisches Set 2 Entspricht dem OpenType-Tag: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Stilistisches Set 3 Entspricht dem OpenType-Tag: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Stilistisches Set 4 Entspricht dem OpenType-Tag: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Stilistisches Set 5 Entspricht dem OpenType-Tag: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Stilistisches Set 6 Entspricht dem OpenType-Tag: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Stilistisches Set 7 Entspricht dem OpenType-Tag: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Stilistisches Set 8 Entspricht dem OpenType-Tag: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Stilistisches Set 9 Entspricht dem OpenType-Tag: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Stilistisches Set 10 Entspricht dem OpenType-Tag: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Stilistisches Set 11 Entspricht dem OpenType-Tag: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Stilistisches Set 12 Entspricht dem OpenType-Tag: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Stilistisches Set 13 Entspricht dem OpenType-Tag: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Stilistisches Set 14 Entspricht dem OpenType-Tag: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Stilistisches Set 15 Entspricht dem OpenType-Tag: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Stilistisches Set 16 Entspricht dem OpenType-Tag: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Stilistisches Set 17 Entspricht dem OpenType-Tag: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Stilistisches Set 18 Entspricht dem OpenType-Tag: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Stilistisches Set 19 Entspricht dem OpenType-Tag: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Stilistisches Set 20 Entspricht dem OpenType-Tag: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Ersetzt Ziffern‑Glyphen, die in proportionalen Breiten gesetzt sind, durch entsprechende Glyphen, die in einheitlichen (tabellarischen) Breiten gesetzt sind. |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Wandelt Standards‑Glyphen in Glyphen um, die für die aufrechte Darstellung im vertikalen Schreibmodus geeignet sind. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Ersetzt einige festbreite (halb‑, dritt‑ oder viertelbreite) oder proportional‑breite Glyphen (hauptsächlich Lateinisch oder Katakana) durch Formen, die für das vertikale Schreiben geeignet sind (d. h. um 90 Grad im Uhrzeigersinn gedreht). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Im Gegensatz zu anderen Ligatur‑Features gibt 'clig' den Kontext an, in dem die Ligatur empfohlen wird. Diese Fähigkeit ist in einigen Schriftsystem‑Entwürfen und für Schwung‑Ligaturen wichtig. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Entspricht dem OpenType-Tag: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Ersetzt eine Sequenz von Glyphen durch ein einzeltes Glyph, das für typografische Zwecke bevorzugt wird. Dieses Feature umfasst jene Ligaturen, die für Sonderwirkungen verwendet werden können, nach Wunsch des Benutzers. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Entspricht dem OpenType-Tag: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


Um die Anzahl der Glyphen‑Alternativen zu minimieren, ist es manchmal wünschenswert, das Standardglyph für ein Zeichen in zwei oder mehr Glyphen zu zerlegen. Zusätzlich kann es vorzuziehen sein, Standardglyphen für zwei oder mehr Zeichen zu einem einzigen Glyphen zusammenzusetzen, um die Glyphenverarbeitung zu verbessern. Diese Funktion ermöglicht solche Zusammensetzung/Zerlegung. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_ae\\#ccmp Equivalent OpenType tag: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Einige Ligaturen waren in der Vergangenheit gebräuchlich, wirken heute jedoch anachronistisch. Einige Schriftarten enthalten die historischen Formen als Alternativen, sodass sie für einen "Perioden"‑Effekt verwendet werden können. Diese Funktion ersetzt die Standard‑ (aktuellen) Formen durch die historischen Alternativen. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_fj\\#hlig Equivalent OpenType tag: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Passt den Abstand zwischen Glyphen an, um im Allgemeinen optisch konsistente Abstände zwischen Glyphen zu gewährleisten. Obwohl eine gut gestaltete Schriftart insgesamt konsistente Zwischen‑Glyphen‑Abstände hat, erfordern einige Glyphenkombinationen eine Anpassung für bessere Lesbarkeit. Neben der Standardanpassung in horizontaler Richtung kann diese Funktion größenabhängige Kerning‑Daten über Gerätetabellen bereitstellen, "cross‑stream"‑Kerning in Y‑Textrichtung und die Anpassung der Glyphenposition unabhängig von der Vorwärts‑Anpassung. Hinweis: Diese Funktion kann auf Laufketten von mehr als zwei Glyphen angewendet werden und würde in monospaced Schriften nicht verwendet werden. Außerdem gilt diese Funktion nicht für vertikal gesetzten Text. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_ko\\#kern Equivalent OpenType tag: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


Diese Funktion ändert ausgewählte nicht‑linierende Ziffern in linierende Ziffern. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_ko\\#lnum Equivalent OpenType tag: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


Diese Funktion ändert ausgewählte Ziffern vom Standard‑ oder linierenden Stil in die Alt‑Ziffern‑Form. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_ko\\#onum Equivalent OpenType tag: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Ersetzt Ziffernglyphen mit einheitlicher (tabellarischer) Breite durch entsprechende Glyphen mit glyph‑spezifischer (proportionaler) Breite. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_pt\\#tag-pnum Equivalent OpenType tag: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Ersetzt eine Sequenz von Glyphen durch ein einzelnes Glyph, das für typografische Zwecke bevorzugt wird. Diese Funktion umfasst jene Ligaturen, die das Schriftsystem als in normalen Bedingungen erforderlich bestimmt. Diese Funktion ist für einige Schriftsysteme wichtig, um eine korrekte Glyphenbildung sicherzustellen. https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_pt\\#rlig Equivalent OpenType tag: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Ersetzt eine Sequenz von Glyphen durch ein einzeltes Glyph, das für typografische Zwecke bevorzugt wird. Diese Funktion umfasst die Ligaturen, die der Designer/Hersteller für den Einsatz unter normalen Bedingungen hält. Equivalent OpenType tag: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\\_ko\\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Stylistic Set 1 Zusätzlich zu oder anstelle von stilistischen Alternativen einzelner Glyphen (siehe 'salt'-Feature), können einige Schriftarten Sets von stilistischen Varianten‑Glyphen enthalten, die sich auf Teile des Zeichensatzes beziehen, z. B. mehrere Varianten für Kleinbuchstaben in einer lateinischen Schrift. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 Entsprechender OpenType‑Tag: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Stilistisches Set 2 Entspricht dem OpenType-Tag: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Stilistisches Set 3 Entspricht dem OpenType-Tag: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Stilistisches Set 4 Entspricht dem OpenType-Tag: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Stilistisches Set 5 Entspricht dem OpenType-Tag: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Stilistisches Set 6 Entspricht dem OpenType-Tag: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Stilistisches Set 7 Entspricht dem OpenType-Tag: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Stilistisches Set 8 Entspricht dem OpenType-Tag: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Stilistisches Set 9 Entspricht dem OpenType-Tag: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Stilistisches Set 10 Entspricht dem OpenType-Tag: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Stilistisches Set 11 Entspricht dem OpenType-Tag: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Stilistisches Set 12 Entspricht dem OpenType-Tag: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Stilistisches Set 13 Entspricht dem OpenType-Tag: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Stilistisches Set 14 Entspricht dem OpenType-Tag: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Stilistisches Set 15 Entspricht dem OpenType-Tag: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Stilistisches Set 16 Entspricht dem OpenType-Tag: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Stilistisches Set 17 Entspricht dem OpenType-Tag: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Stilistisches Set 18 Entspricht dem OpenType-Tag: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Stilistisches Set 19 Entspricht dem OpenType-Tag: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Stilistisches Set 20 Entspricht dem OpenType-Tag: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Ersetzt Ziffern‑Glyphen, die in proportionalen Breiten gesetzt sind, durch entsprechende Glyphen in einheitlichen (tabellarischen) Breiten. Tabellarische Breiten sind in der Regel die Vorgabe, aber das kann nicht sicher angenommen werden. Natürlich würde dieses Feature in monospaced‑Designs nicht vorhanden sein. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum Entsprechender OpenType‑Tag: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Wandelt Standards‑Glyphen in Glyphen um, die für die aufrechte Darstellung im vertikalen Schreibmodus geeignet sind. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert Entsprechender OpenType‑Tag: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Ersetzt einige festbreite (halb‑, dritt‑ oder viertel‑Breite) oder proportional‑breite Glyphen (hauptsächlich Lateinisch oder Katakana) durch Formen, die für das vertikale Schreiben geeignet sind (d. h. um 90 Grad im Uhrzeigersinn gedreht). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 Entsprechender OpenType‑Tag: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
