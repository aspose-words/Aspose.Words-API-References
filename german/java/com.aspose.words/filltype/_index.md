---
title: "FillType"
linktitle: "FillType"
second_title: "Aspose.Words für Java"
description: "Gibt den Fülltyp für ein ausfüllbares Objekt in Java an."
type: docs
weight: 312
url: /de/java/com.aspose.words/filltype/
---

**Inheritance:**
java.lang.Object
```
public class FillType
```

Gibt den Fülltyp für ein ausfüllbares Objekt an.

 **Examples:** 

Zeigt, wie man beliebige Füllungen zurück in eine Vollfarbe konvertiert.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BACKGROUND](#BACKGROUND) | Füllung ist dieselbe wie der Hintergrund. |
| [GRADIENT](#GRADIENT) | Verlaufsfüllung. |
| [PATTERNED](#PATTERNED) | Musterfüllung. |
| [PICTURE](#PICTURE) | Bildfüllung. |
| [SOLID](#SOLID) | Einfarbige Füllung. |
| [TEXTURED](#TEXTURED) | Texturfüllung. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String fillTypeName)](#fromName-java.lang.String) |  |
| [getName(int fillType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fillType)](#toString-int) |  |
### BACKGROUND {#BACKGROUND}
```
public static int BACKGROUND
```


Füllung ist dieselbe wie der Hintergrund.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Verlaufsfüllung.

### PATTERNED {#PATTERNED}
```
public static int PATTERNED
```


Musterfüllung.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Bildfüllung.

### SOLID {#SOLID}
```
public static int SOLID
```


Einfarbige Füllung.

### TEXTURED {#TEXTURED}
```
public static int TEXTURED
```


Texturfüllung.

### length {#length}
```
public static int length
```


### fromName(String fillTypeName) {#fromName-java.lang.String}
```
public static int fromName(String fillTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fillTypeName | java.lang.String |  |

**Returns:**
int
### getName(int fillType) {#getName-int}
```
public static String getName(int fillType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fillType | int |  |

**Returns:**
java.lang.String
