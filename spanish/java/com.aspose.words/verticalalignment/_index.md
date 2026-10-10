---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación vertical de un marco de texto de forma flotante o una tabla flotante en Java."
type: docs
weight: 713
url: /es/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Especifica la alineación vertical de una forma flotante, un marco de texto o una tabla flotante.

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
| [BOTTOM](#BOTTOM) | Especifica que el objeto debe estar en la parte inferior de la base de alineación vertical. |
| [CENTER](#CENTER) | Especifica que el objeto debe estar centrado con respecto a la base de alineación vertical. |
| [DEFAULT](#DEFAULT) | Igual que [NONE](../../com.aspose.words/verticalalignment/\#NONE). |
| [INLINE](#INLINE) | No documentado. |
| [INSIDE](#INSIDE) | Especifica que el objeto debe estar dentro de la base de alineación horizontal. |
| [NONE](#NONE) | El objeto está posicionado explícitamente, normalmente usando su propiedad **Top**. |
| [OUTSIDE](#OUTSIDE) | Especifica que el objeto debe estar fuera de la base de alineación vertical. |
| [TOP](#TOP) | Especifica que el objeto debe estar en la parte superior de la base de alineación vertical. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Especifica que el objeto debe estar en la parte inferior de la base de alineación vertical.

### CENTER {#CENTER}
```
public static int CENTER
```


Especifica que el objeto debe estar centrado con respecto a la base de alineación vertical.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Igual que [NONE](../../com.aspose.words/verticalalignment/\#NONE).

### INLINE {#INLINE}
```
public static int INLINE
```


No documentado. Parece ser un valor posible para párrafos y tablas flotantes.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Especifica que el objeto debe estar dentro de la base de alineación horizontal.

### NONE {#NONE}
```
public static int NONE
```


El objeto está posicionado explícitamente, normalmente usando su propiedad **Top**.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Especifica que el objeto debe estar fuera de la base de alineación vertical.

### TOP {#TOP}
```
public static int TOP
```


Especifica que el objeto debe estar en la parte superior de la base de alineación vertical.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
