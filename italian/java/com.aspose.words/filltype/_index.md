---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di riempimento per un oggetto riempibile in Java."
type: docs
weight: 312
url: /it/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Specifica il tipo di riempimento per un oggetto riempibile.

 **Examples:** 

Mostra come convertire qualsiasi riempimento nuovamente in un riempimento solido.

```

 Document doc = new Document(getMyDir() + "Two color gradient.docx");

 // Get Fill object for Font of the first Run.
 Fill fill = doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).getFont().getFill();

 // Check Fill properties of the Font.
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill is transparent at {0}%",fill.getTransparency() * 100.0));

 // Change type of the fill to Solid with uniform green color.
 fill.solid(Color.GREEN);
 System.out.println("\nThe fill is changed:");
 System.out.println(MessageFormat.format("The type of the fill is: {0}",fill.getFillType()));
 System.out.println(MessageFormat.format("The foreground color of the fill is: {0}",fill.getForeColor()));
 System.out.println(MessageFormat.format("The fill transparency is {0}%",fill.getTransparency() * 100.0));

 doc.save(getArtifactsDir() + "Drawing.FillSolid.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Il riempimento è lo stesso dello sfondo. |
| [GRADIENT](#GRADIENT) | Riempimento gradiente. |
| [PATTERNED](#PATTERNED) | Riempimento a trama. |
| [PICTURE](#PICTURE) | Riempimento immagine. |
| [SOLID](#SOLID) | Riempimento solido. |
| [TEXTURED](#TEXTURED) | Riempimento testurizzato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Il riempimento è lo stesso dello sfondo.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Riempimento gradiente.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Riempimento a trama.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Riempimento immagine.

### SOLID {#SOLID}
```
public static int SOLID
```


Riempimento solido.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Riempimento testurizzato.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fillType) {#toString-int}
```
public static String toString(int fillType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
