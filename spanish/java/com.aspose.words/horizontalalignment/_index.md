---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación horizontal de un marco de texto de forma flotante o una tabla flotante en Java."
type: docs
weight: 374
url: /es/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Especifica la alineación horizontal de una forma flotante, marco de texto o tabla flotante.

 **Examples:** 

Muestra cómo insertar una imagen flotante en el centro de una página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTER](#CENTER) | Especifica que el objeto debe estar centrado con respecto a la base de alineación horizontal. |
| [DEFAULT](#DEFAULT) | Igual que [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Especifica que el objeto debe estar dentro de la base de alineación horizontal. |
| [LEFT](#LEFT) | Especifica que el objeto debe alinearse a la izquierda con la base de alineación horizontal. |
| [NONE](#NONE) | El objeto está posicionado explícitamente, normalmente usando su propiedad **Left**. |
| [OUTSIDE](#OUTSIDE) | Especifica que el objeto debe estar fuera de la base de alineación horizontal. |
| [RIGHT](#RIGHT) | Especifica que el objeto debe alinearse a la derecha con la base de alineación horizontal. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Especifica que el objeto debe estar centrado con respecto a la base de alineación horizontal.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Igual que [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Especifica que el objeto debe estar dentro de la base de alineación horizontal.

### LEFT {#LEFT}
```
public static int LEFT
```


Especifica que el objeto debe alinearse a la izquierda con la base de alineación horizontal.

### NONE {#NONE}
```
public static int NONE
```


El objeto está posicionado explícitamente, normalmente usando su propiedad **Left**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Especifica que el objeto debe estar fuera de la base de alineación horizontal.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Especifica que el objeto debe alinearse a la derecha con la base de alineación horizontal.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
