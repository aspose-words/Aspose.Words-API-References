---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words für Java"
description: "Gibt mögliche Typen von Betonungszeichen in Java an."
type: docs
weight: 187
url: /de/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Gibt mögliche Typen von Betonungszeichen an.

 **Examples:** 

Zeigt, wie man ein zusätzliches Zeichen hinzufügt, das über/unter dem Glyphen‑Zeichen dargestellt wird.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [NONE](#NONE) | Keine Betonungsmarke. |
| [OVER_COMMA](#OVER-COMMA) | Die Betonungsmarke ist ein Komma‑Zeichen, das über dem Text angezeigt wird. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Die Betonungsmarke ist ein durchgehender schwarzer Kreis, der über dem Text angezeigt wird. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Die Betonungsmarke ist ein leerer weißer Kreis, der über dem Text angezeigt wird. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Die Betonungsmarke ist ein durchgehender schwarzer Kreis, der unter dem Text angezeigt wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Keine Betonungsmarke.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Die Betonungsmarke ist ein Komma‑Zeichen, das über dem Text angezeigt wird.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Die Betonungsmarke ist ein durchgehender schwarzer Kreis, der über dem Text angezeigt wird.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Die Betonungsmarke ist ein leerer weißer Kreis, der über dem Text angezeigt wird.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Die Betonungsmarke ist ein durchgehender schwarzer Kreis, der unter dem Text angezeigt wird.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
