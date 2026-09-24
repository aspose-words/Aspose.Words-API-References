---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words para Java"
description: "Las características proporcionan información sobre cómo se utilizan los glifos en una fuente para representar un script en Java."
type: docs
weight: 325
url: /es/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Las características proporcionan información sobre cómo se utilizan los glifos en una fuente para representar un script. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Campos

| Campo | Descripción |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | Para minimizar el número de variantes de glifos, a veces es deseable descomponer el glifo predeterminado de un carácter en dos o más glifos. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Algunas ligaduras se usaban comúnmente en el pasado, pero hoy parecen anacrónicas. |
| [KERNING](#KERNING) | Ajusta la cantidad de espacio entre glifos, generalmente para proporcionar un espaciado ópticamente consistente entre glifos. |
| [LINING_FIGURES](#LINING-FIGURES) | Esta característica cambia las figuras no alineadas seleccionadas a figuras alineadas. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | Esta característica cambia las figuras seleccionadas del estilo predeterminado o alineado a la forma de estilo antiguo. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Reemplaza los glifos de figuras establecidos en anchos uniformes (tabulares) con los glifos correspondientes establecidos en anchos específicos de glifo (proporcionales). |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Stylistic Set 1 Además de, o en lugar de, alternativas estilísticas de glifos individuales (ver la característica 'salt'), algunas fuentes pueden contener conjuntos de glifos variantes estilísticas correspondientes a porciones del conjunto de caracteres, p. ej. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Stylistic Set 2 Etiqueta OpenType equivalente: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Stylistic Set 3 Etiqueta OpenType equivalente: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Stylistic Set 4 Etiqueta OpenType equivalente: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Stylistic Set 5 Etiqueta OpenType equivalente: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Stylistic Set 6 Etiqueta OpenType equivalente: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Stylistic Set 7 Etiqueta OpenType equivalente: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Stylistic Set 8 Etiqueta OpenType equivalente: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Stylistic Set 9 Etiqueta OpenType equivalente: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Stylistic Set 10 Etiqueta OpenType equivalente: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Stylistic Set 11 Etiqueta OpenType equivalente: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Stylistic Set 12 Etiqueta OpenType equivalente: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Stylistic Set 13 Etiqueta OpenType equivalente: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Stylistic Set 14 Etiqueta OpenType equivalente: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Stylistic Set 15 Etiqueta OpenType equivalente: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Stylistic Set 16 Etiqueta OpenType equivalente: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Stylistic Set 17 Etiqueta OpenType equivalente: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Stylistic Set 18 Etiqueta OpenType equivalente: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Stylistic Set 19 Etiqueta OpenType equivalente: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Conjunto estilístico 20 Etiqueta OpenType equivalente: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Reemplaza los glifos de cifras establecidos en anchos proporcionales con los glifos correspondientes establecidos en anchos uniformes (tabulares). |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Transforma los glifos predeterminados en glifos apropiados para una presentación vertical en modo de escritura vertical. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Reemplaza algunos glifos de ancho fijo (media, un tercio o un cuarto de ancho) o de ancho proporcional (principalmente latinos o katakana) con formas adecuadas para la escritura vertical (es decir, rotados 90 grados en sentido horario). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. A diferencia de otras características de ligadura, 'clig' especifica el contexto en el que se recomienda la ligadura. Esta capacidad es importante en algunos diseños de escritura y para ligaduras con remates. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Equivalent OpenType tag: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. Esta característica cubre aquellas ligaduras que pueden usarse para efectos especiales, a preferencia del usuario\u2019s. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Equivalent OpenType tag: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


Para minimizar el número de alternancias de glifos, a veces es deseable descomponer el glifo predeterminado de un carácter en dos o más glifos. Además, puede ser preferible componer glifos predeterminados de dos o más caracteres en un solo glifo para un mejor procesamiento de glifos. Esta característica permite dicha composición/descomposición. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp Equivalent OpenType tag: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Algunas ligaduras estaban en uso común en el pasado, pero hoy parecen anacrónicas. Algunas fuentes incluyen las formas históricas como alternantes, de modo que pueden usarse para un efecto de "period". Esta característica reemplaza las formas predeterminadas (actuales) con las alternantes históricas. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig Equivalent OpenType tag: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Ajusta la cantidad de espacio entre glifos, generalmente para proporcionar un espaciado ópticamente consistente entre glifos. Aunque una tipografía bien diseñada tiene un espaciado interglifo consistente en general, algunas combinaciones de glifos requieren ajuste para mejorar la legibilidad. Además del ajuste estándar en la dirección horizontal, esta característica puede suministrar datos de kerning dependientes del tamaño mediante tablas de dispositivos, kerning "cross-stream" en la dirección Y del texto, y ajuste de la posición del glifo independiente del ajuste de avance. Tenga en cuenta que esta característica puede aplicarse a secuencias de más de dos glifos, y no se usaría en fuentes monoespaciadas. También tenga en cuenta que esta característica no se aplica al texto dispuesto verticalmente. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern Equivalent OpenType tag: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


Esta característica cambia las cifras no alineadas seleccionadas a cifras alineadas. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum Equivalent OpenType tag: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


Esta característica cambia las cifras seleccionadas del estilo predeterminado o alineado a la forma de estilo antiguo. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum Equivalent OpenType tag: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Reemplaza los glifos de cifras establecidos en anchos uniformes (tabulares) con los glifos correspondientes establecidos en anchos específicos del glifo (proporcionales). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum Equivalent OpenType tag: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. Esta característica cubre aquellas ligaduras que la escritura determina como necesarias para usarse en condiciones normales. Esta característica es importante para algunas escrituras para asegurar la formación correcta de glifos. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig Equivalent OpenType tag: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Reemplaza una secuencia de glifos con un solo glifo que se prefiere para propósitos tipográficos. Esta característica cubre las ligaduras que el diseñador/fabricante considera que deben usarse en condiciones normales. Etiqueta OpenType equivalente: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Conjunto estilístico 1 Además de, o en lugar de, alternativas estilísticas de glifos individuales (ver característica 'salt'), algunas fuentes pueden contener conjuntos de glifos variantes estilísticas que corresponden a porciones del conjunto de caracteres, p. ej., múltiples variantes para letras minúsculas en una fuente latina. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 Etiqueta OpenType equivalente: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Stylistic Set 2 Etiqueta OpenType equivalente: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Stylistic Set 3 Etiqueta OpenType equivalente: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Stylistic Set 4 Etiqueta OpenType equivalente: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Stylistic Set 5 Etiqueta OpenType equivalente: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Stylistic Set 6 Etiqueta OpenType equivalente: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Stylistic Set 7 Etiqueta OpenType equivalente: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Stylistic Set 8 Etiqueta OpenType equivalente: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Stylistic Set 9 Etiqueta OpenType equivalente: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Stylistic Set 10 Etiqueta OpenType equivalente: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Stylistic Set 11 Etiqueta OpenType equivalente: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Stylistic Set 12 Etiqueta OpenType equivalente: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Stylistic Set 13 Etiqueta OpenType equivalente: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Stylistic Set 14 Etiqueta OpenType equivalente: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Stylistic Set 15 Etiqueta OpenType equivalente: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Stylistic Set 16 Etiqueta OpenType equivalente: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Stylistic Set 17 Etiqueta OpenType equivalente: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Stylistic Set 18 Etiqueta OpenType equivalente: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Stylistic Set 19 Etiqueta OpenType equivalente: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Conjunto estilístico 20 Etiqueta OpenType equivalente: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Reemplaza los glifos de figuras con anchos proporcionales por los glifos correspondientes con anchos uniformes (tabulares). Los anchos tabulares generalmente serán el predeterminado, pero no se puede asumir con seguridad. Por supuesto, esta característica no estaría presente en diseños monoespaciados. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum Etiqueta OpenType equivalente: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Transforma los glifos predeterminados en glifos apropiados para presentación vertical en modo de escritura vertical. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert Etiqueta OpenType equivalente: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Reemplaza algunos glifos de ancho fijo (media, un tercio o un cuarto de ancho) o de ancho proporcional (principalmente latinos o katakana) con formas adecuadas para escritura vertical (es decir, rotados 90 grados en sentido horario). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 Etiqueta OpenType equivalente: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
