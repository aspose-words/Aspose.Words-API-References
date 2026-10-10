---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words para Java"
description: "Especifica los posibles tipos de marca de énfasis en Java."
type: docs
weight: 187
url: /es/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Especifica los tipos posibles de marca de énfasis.

 **Examples:** 

Muestra cómo agregar un carácter adicional renderizado arriba/abajo del glifo-carácter.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | Sin marca de énfasis. |
| [OVER_COMMA](#OVER-COMMA) | La marca de énfasis es un carácter de coma que se muestra encima del texto. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | La marca de énfasis es un círculo negro sólido que se muestra encima del texto. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | La marca de énfasis es un círculo blanco vacío que se muestra encima del texto. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | La marca de énfasis es un círculo negro sólido que se muestra debajo del texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Sin marca de énfasis.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


La marca de énfasis es un carácter de coma que se muestra encima del texto.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


La marca de énfasis es un círculo negro sólido que se muestra encima del texto.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


La marca de énfasis es un círculo blanco vacío que se muestra encima del texto.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


La marca de énfasis es un círculo negro sólido que se muestra debajo del texto.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
