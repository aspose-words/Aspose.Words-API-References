---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words per Java"
description: "Le funzionalità forniscono informazioni su come i glifi sono usati in un carattere per renderizzare una scrittura in Java."
type: docs
weight: 325
url: /it/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

Le funzionalità forniscono informazioni su come i glifi sono usati in un carattere per renderizzare una scrittura. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## Campi

| Campo | Descrizione |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | Per ridurre al minimo il numero di varianti di glifi, a volte è desiderabile scomporre il glifo predefinito di un carattere in due o più glifi. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | Alcune legature erano di uso comune in passato, ma oggi appaiono anacronistiche. |
| [KERNING](#KERNING) | Regola la quantità di spazio tra i glifi, generalmente per fornire una spaziatura otticamente coerente tra i glifi. |
| [LINING_FIGURES](#LINING-FIGURES) | Questa funzione trasforma le cifre non allineate selezionate in cifre allineate. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | Questa funzione trasforma le cifre selezionate dallo stile predefinito o allineato alla forma antica. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | Sostituisce i glifi delle cifre impostati su larghezze uniformi (tabulari) con i corrispondenti glifi impostati su larghezze specifiche per glifo (proporzionali). |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | Set Stilistico 1 Oltre a, o al posto di, alternative stilistiche di glifi individuali (vedi la funzione 'salt'), alcuni caratteri possono contenere insiemi di glifi varianti stilistici corrispondenti a parti del set di caratteri, ad es. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | Set Stilistico 2 Tag OpenType equivalente: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | Set Stilistico 3 Tag OpenType equivalente: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | Set Stilistico 4 Tag OpenType equivalente: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | Set Stilistico 5 Tag OpenType equivalente: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | Set Stilistico 6 Tag OpenType equivalente: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | Set Stilistico 7 Tag OpenType equivalente: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | Set Stilistico 8 Tag OpenType equivalente: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | Set Stilistico 9 Tag OpenType equivalente: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | Set Stilistico 10 Tag OpenType equivalente: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | Set Stilistico 11 Tag OpenType equivalente: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | Set Stilistico 12 Tag OpenType equivalente: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | Set Stilistico 13 Tag OpenType equivalente: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | Set Stilistico 14 Tag OpenType equivalente: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | Set Stilistico 15 Tag OpenType equivalente: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | Set Stilistico 16 Tag OpenType equivalente: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | Set Stilistico 17 Tag OpenType equivalente: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | Set Stilistico 18 Tag OpenType equivalente: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | Set Stilistico 19 Tag OpenType equivalente: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | Set stilistico 20 Tag OpenType equivalente: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | Sostituisce i glifi delle cifre impostati su larghezze proporzionali con i glifi corrispondenti impostati su larghezze uniformi (tabulari). |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | Trasforma i glifi predefiniti in glifi appropriati per una presentazione verticale in modalità di scrittura verticale. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | Sostituisce alcuni glifi a larghezza fissa (metà, un terzo o un quarto) o a larghezza proporzionale (principalmente latini o katakana) con forme adatte alla scrittura verticale (cioè ruotati di 90 gradi in senso orario). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


Sostituisce una sequenza di glifi con un singolo glifo preferito per scopi tipografici. A differenza di altre funzionalità di legatura, 'clig' specifica il contesto in cui la legatura è consigliata. Questa capacità è importante in alcuni progetti di scrittura e per le legature decorative. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig Equivalent OpenType tag: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


Sostituisce una sequenza di glifi con un singolo glifo preferito per scopi tipografici. Questa funzionalità copre le legature che possono essere usate per effetti speciali, a discrezione dell'utente. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig Equivalent OpenType tag: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


Per ridurre al minimo il numero di alternative di glifi, a volte è desiderabile scomporre il glifo predefinito di un carattere in due o più glifi. Inoltre, può essere preferibile comporre i glifi predefiniti di due o più caratteri in un unico glifo per una migliore elaborazione dei glifi. Questa funzionalità consente tale composizione/scomposizione. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp Equivalent OpenType tag: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


Alcune legature erano di uso comune in passato, ma oggi appaiono anacronistiche. Alcuni caratteri includono le forme storiche come alternative, così possono essere usate per un effetto "d'epoca". Questa funzionalità sostituisce le forme predefinite (attuali) con le alternative storiche. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig Equivalent OpenType tag: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


Regola la quantità di spazio tra i glifi, generalmente per fornire una spaziatura otticamente coerente tra i glifi. Sebbene un carattere ben progettato abbia una spaziatura inter-glifi coerente in generale, alcune combinazioni di glifi richiedono una regolazione per migliorare la leggibilità. Oltre alla regolazione standard nella direzione orizzontale, questa funzionalità può fornire dati di kerning dipendenti dalla dimensione tramite tabelle dispositivo, kerning "cross-stream" nella direzione verticale (asse Y) del testo, e regolazione del posizionamento dei glifi indipendente dalla regolazione dell'avanzamento. Si noti che questa funzionalità può applicarsi a sequenze di più di due glifi e non verrebbe usata nei caratteri a larghezza fissa. Si noti inoltre che questa funzionalità non si applica al testo impostato verticalmente. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern Equivalent OpenType tag: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


Questa funzionalità trasforma le cifre non allineate selezionate in cifre allineate. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum Equivalent OpenType tag: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


Questa funzionalità trasforma le cifre selezionate dallo stile predefinito o allineato a forma oldstyle. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum Equivalent OpenType tag: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


Sostituisce i glifi delle cifre impostati su larghezze uniformi (tabulari) con i glifi corrispondenti impostati su larghezze specifiche per glifo (proporzionali). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum Equivalent OpenType tag: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


Sostituisce una sequenza di glifi con un singolo glifo preferito per scopi tipografici. Questa funzionalità copre le legature che lo script determina necessarie da usare in condizioni normali. Questa funzionalità è importante per alcuni script per garantire la corretta formazione dei glifi. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig Equivalent OpenType tag: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


Sostituisce una sequenza di glifi con un singolo glifo preferito per scopi tipografici. Questa funzionalità copre le legature che il progettista/fabbricante ritiene debbano essere usate in condizioni normali. Equivalent OpenType tag: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


Set stilistico 1 Oltre a, o al posto di, alternative stilistiche di singoli glifi (vedi 'salt' feature), alcuni font possono contenere insiemi di glifi varianti stilistiche corrispondenti a parti del set di caratteri, ad esempio più varianti per le lettere minuscole in un font latino. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 Equivalent OpenType tag: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


Set Stilistico 2 Tag OpenType equivalente: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


Set Stilistico 3 Tag OpenType equivalente: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


Set Stilistico 4 Tag OpenType equivalente: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


Set Stilistico 5 Tag OpenType equivalente: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


Set Stilistico 6 Tag OpenType equivalente: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


Set Stilistico 7 Tag OpenType equivalente: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


Set Stilistico 8 Tag OpenType equivalente: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


Set Stilistico 9 Tag OpenType equivalente: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


Set Stilistico 10 Tag OpenType equivalente: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


Set Stilistico 11 Tag OpenType equivalente: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


Set Stilistico 12 Tag OpenType equivalente: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


Set Stilistico 13 Tag OpenType equivalente: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


Set Stilistico 14 Tag OpenType equivalente: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


Set Stilistico 15 Tag OpenType equivalente: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


Set Stilistico 16 Tag OpenType equivalente: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


Set Stilistico 17 Tag OpenType equivalente: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


Set Stilistico 18 Tag OpenType equivalente: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


Set Stilistico 19 Tag OpenType equivalente: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


Set stilistico 20 Tag OpenType equivalente: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


Sostituisce i glifi numerici impostati su larghezze proporzionali con i glifi corrispondenti impostati su larghezze uniformi (tabulari). Le larghezze tabulari saranno generalmente predefinite, ma non si può presumere in modo sicuro. Naturalmente questa funzionalità non sarebbe presente nei progetti monospaziati. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum Equivalent OpenType tag: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


Trasforma i glifi predefiniti in glifi appropriati per una presentazione verticale in modalità di scrittura verticale. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert Equivalent OpenType tag: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


Sostituisce alcuni glifi a larghezza fissa (metà, un terzo o un quarto) o a larghezza proporzionale (principalmente latini o katakana) con forme adatte alla scrittura verticale (cioè ruotati di 90 gradi in senso orario). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 Equivalent OpenType tag: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
