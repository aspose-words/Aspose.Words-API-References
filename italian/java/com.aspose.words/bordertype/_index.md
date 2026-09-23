---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words per Java"
description: "Specifica i lati di un bordo in Java."
type: docs
weight: 48
url: /it/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Specifica i lati di un bordo.

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Examples:** 

Mostra come inserire un paragrafo con un bordo superiore.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM](#BOTTOM) | Specifica il bordo inferiore di un paragrafo o di una cella di tabella. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Specifica il bordo diagonale in una cella di tabella. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Specifica il bordo diagonale in una cella di tabella. |
| [HORIZONTAL](#HORIZONTAL) | Specifica il bordo orizzontale tra le celle in una tabella o tra paragrafi conformi. |
| [LEFT](#LEFT) | Specifica il bordo sinistro di un paragrafo o di una cella di tabella. |
| [NONE](#NONE) | Valore predefinito. |
| [RIGHT](#RIGHT) | Specifica il bordo destro di un paragrafo o di una cella di tabella. |
| [TOP](#TOP) | Specifica il bordo superiore di un paragrafo o di una cella di tabella. |
| [VERTICAL](#VERTICAL) | Specifica il bordo verticale tra le celle in una tabella. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifica il bordo inferiore di un paragrafo o di una cella di tabella.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Specifica il bordo diagonale in una cella di tabella.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Specifica il bordo diagonale in una cella di tabella.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Specifica il bordo orizzontale tra le celle in una tabella o tra paragrafi conformi.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifica il bordo sinistro di un paragrafo o di una cella di tabella.

### NONE {#NONE}
```
public static int NONE
```


Valore predefinito.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifica il bordo destro di un paragrafo o di una cella di tabella.

### TOP {#TOP}
```
public static int TOP
```


Specifica il bordo superiore di un paragrafo o di una cella di tabella.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Specifica il bordo verticale tra le celle in una tabella.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
