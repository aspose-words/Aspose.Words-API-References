---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words pour Java"
description: "Les fonctionnalités fournissent des informations sur la façon dont les glyphes sont utilisés dans une police pour rendre un script en Java."
type: docs
weight: 325
url: /fr/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Les fonctionnalités fournissent des informations sur la façon dont les glyphes sont utilisés dans une police pour rendre un script. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Champs

| Champ | Description |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | Pour minimiser le nombre d'alternatives de glyphes, il est parfois souhaitable de décomposer le glyphe par défaut d'un caractère en deux ou plusieurs glyphes. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Certaines ligatures étaient couramment utilisées dans le passé, mais semblent anachroniques aujourd'hui. |
| [KERNING](#KERNING) | Ajuste la quantité d'espace entre les glyphes, généralement pour fournir un espacement optiquement cohérent entre les glyphes. |
| [LINING_FIGURES](#LINING-FIGURES) | Cette fonctionnalité convertit les chiffres non alignés sélectionnés en chiffres alignés. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | Cette fonctionnalité convertit les chiffres sélectionnés du style par défaut ou aligné en forme ancienne. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Remplace les glyphes de chiffres définis sur des largeurs uniformes (tabulaires) par les glyphes correspondants définis sur des largeurs spécifiques aux glyphes (proportionnelles). |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Stylistic Set 1 En plus de, ou à la place des alternatives stylistiques de glyphes individuels (voir la fonctionnalité 'salt'), certaines polices peuvent contenir des ensembles de glyphes variantes stylistiques correspondant à des parties du jeu de caractères, par ex. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Stylistic Set 2 Équivalent de la balise OpenType : 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Stylistic Set 3 Équivalent de la balise OpenType : 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Stylistic Set 4 Équivalent de la balise OpenType : 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Stylistic Set 5 Équivalent de la balise OpenType : 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Stylistic Set 6 Équivalent de la balise OpenType : 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Stylistic Set 7 Équivalent de la balise OpenType : 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Stylistic Set 8 Équivalent de la balise OpenType : 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Stylistic Set 9 Équivalent de la balise OpenType : 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Stylistic Set 10 Équivalent de la balise OpenType : 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Stylistic Set 11 Équivalent de la balise OpenType : 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Stylistic Set 12 Équivalent de la balise OpenType : 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Stylistic Set 13 Équivalent de la balise OpenType : 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Stylistic Set 14 Équivalent de la balise OpenType : 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Stylistic Set 15 Équivalent de la balise OpenType : 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Stylistic Set 16 Équivalent de la balise OpenType : 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Stylistic Set 17 Équivalent de la balise OpenType : 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Stylistic Set 18 Équivalent de la balise OpenType : 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Stylistic Set 19 Équivalent de la balise OpenType : 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Ensemble stylistique 20 Équivalent du tag OpenType : 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Remplace les glyphes de chiffres définis sur des largeurs proportionnelles par les glyphes correspondants définis sur des largeurs uniformes (tabulaires). |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Transforme les glyphes par défaut en glyphes appropriés à une présentation verticale en mode d'écriture verticale. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Remplace certains glyphes à largeur fixe (demi‑largeur, tiers ou quart de largeur) ou à largeur proportionnelle (principalement latins ou katakana) par des formes adaptées à l'écriture verticale (c’est‑à‑dire, tournées de 90 degrés dans le sens des aiguilles d’une montre). |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. Contrairement aux autres fonctionnalités de ligature, 'clig' spécifie le contexte dans lequel la ligature est recommandée. Cette capacité est importante dans certaines conceptions de scripts et pour les ligatures à swash. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Equivalent OpenType tag: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures qui peuvent être utilisées pour un effet spécial, selon la préférence de l\u2019utilisateur. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Equivalent OpenType tag: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


Pour réduire le nombre d’alternatives de glyphes, il est parfois souhaitable de décomposer le glyphe par défaut d’un caractère en deux ou plusieurs glyphes. De plus, il peut être préférable de composer les glyphes par défaut de deux caractères ou plus en un seul glyphe afin d’améliorer le traitement des glyphes. Cette fonctionnalité permet une telle composition/décomposition. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp Equivalent OpenType tag: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Certaines ligatures étaient couramment utilisées par le passé, mais semblent anachroniques aujourd’hui. Certaines polices incluent les formes historiques comme alternatives, afin de pouvoir les utiliser pour un effet "période". Cette fonctionnalité remplace les formes par défaut (actuelles) par les alternatives historiques. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig Equivalent OpenType tag: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Ajuste la quantité d’espace entre les glyphes, généralement pour fournir un espacement optiquement cohérent entre les glyphes. Bien qu’une police bien conçue possède un espacement inter-glyphes globalement constant, certaines combinaisons de glyphes nécessitent un ajustement pour améliorer la lisibilité. En plus de l’ajustement standard dans la direction horizontale, cette fonctionnalité peut fournir des données de crénage dépendantes de la taille via des tables d’appareil, "cross-stream" crénage dans la direction Y du texte, et un ajustement du placement des glyphes indépendant de l’ajustement de l’avance. Notez que cette fonctionnalité peut s’appliquer à des séquences de plus de deux glyphes, et ne serait pas utilisée dans les polices à chasse fixe. Notez également que cette fonctionnalité ne s’applique pas au texte disposé verticalement. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern Equivalent OpenType tag: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


Cette fonctionnalité transforme les chiffres non‑alignés sélectionnés en chiffres alignés. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum Equivalent OpenType tag: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


Cette fonctionnalité transforme les chiffres sélectionnés du style par défaut ou aligné en forme oldstyle. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum Equivalent OpenType tag: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Remplace les glyphes de chiffres définis sur des largeurs uniformes (tabulaires) par les glyphes correspondants définis sur des largeurs spécifiques au glyphe (proportionnelles). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum Equivalent OpenType tag: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Remplace une séquence de glyphes par un seul glyphe qui est préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures que le script détermine comme obligatoires à utiliser dans des conditions normales. Cette fonctionnalité est importante pour certains scripts afin d’assurer une formation correcte des glyphes. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig Equivalent OpenType tag: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Remplace une séquence de glyphes par un seul glyphe, ce qui est préféré à des fins typographiques. Cette fonctionnalité couvre les ligatures que le concepteur/fabricant estime devoir être utilisées dans des conditions normales. Étiquette OpenType équivalente : 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Ensemble stylistique 1 En plus ou à la place des alternatives stylistiques de glyphes individuels (voir la fonctionnalité 'salt'), certaines polices peuvent contenir des ensembles de glyphes variantes stylistiques correspondant à des parties de l’ensemble de caractères, par exemple plusieurs variantes pour les lettres minuscules d’une police latine. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Étiquette OpenType équivalente : 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Stylistic Set 2 Équivalent de la balise OpenType : 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Stylistic Set 3 Équivalent de la balise OpenType : 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Stylistic Set 4 Équivalent de la balise OpenType : 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Stylistic Set 5 Équivalent de la balise OpenType : 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Stylistic Set 6 Équivalent de la balise OpenType : 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Stylistic Set 7 Équivalent de la balise OpenType : 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Stylistic Set 8 Équivalent de la balise OpenType : 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Stylistic Set 9 Équivalent de la balise OpenType : 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Stylistic Set 10 Équivalent de la balise OpenType : 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Stylistic Set 11 Équivalent de la balise OpenType : 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Stylistic Set 12 Équivalent de la balise OpenType : 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Stylistic Set 13 Équivalent de la balise OpenType : 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Stylistic Set 14 Équivalent de la balise OpenType : 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Stylistic Set 15 Équivalent de la balise OpenType : 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Stylistic Set 16 Équivalent de la balise OpenType : 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Stylistic Set 17 Équivalent de la balise OpenType : 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Stylistic Set 18 Équivalent de la balise OpenType : 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Stylistic Set 19 Équivalent de la balise OpenType : 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Ensemble stylistique 20 Équivalent du tag OpenType : 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Remplace les glyphes de chiffres définis en largeurs proportionnelles par les glyphes correspondants définis en largeurs uniformes (tabulaires). Les largeurs tabulaires seront généralement la valeur par défaut, mais cela ne peut pas être supposé en toute sécurité. Bien sûr, cette fonctionnalité ne serait pas présente dans les conceptions à chasse fixe. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Étiquette OpenType équivalente : 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Transforme les glyphes par défaut en glyphes appropriés pour une présentation verticale en mode d’écriture verticale. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Étiquette OpenType équivalente : 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Remplace certains glyphes à chasse fixe (demi‑largeur, tiers ou quart de largeur) ou à chasse proportionnelle (principalement latins ou katakana) par des formes adaptées à l’écriture verticale (c’est‑à‑dire tournées de 90 degrés dans le sens des aiguilles d’une montre). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Étiquette OpenType équivalente : 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
