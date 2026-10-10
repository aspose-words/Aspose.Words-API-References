---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se ajusta el texto alrededor de una forma o imagen en Java."
type: docs
weight: 737
url: /es/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Especifica cómo se envuelve el texto alrededor de una forma o imagen.

 **Examples:** 

Muestra cómo insertar una imagen y usarla como marca de agua.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

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
| [INLINE](#INLINE) | La forma permanece en la misma capa que el texto y se trata como un carácter. |
| [NONE](#NONE) | Sin ajuste de texto alrededor de la forma. |
| [SQUARE](#SQUARE) | Ajusta el texto alrededor de todos los lados del cuadro delimitador cuadrado de la forma. |
| [THROUGH](#THROUGH) | Igual que Tight, pero ajusta dentro de cualquier parte de la forma que esté abierta. |
| [TIGHT](#TIGHT) | Ajusta estrechamente alrededor de los bordes de la forma, en lugar de ajustarse alrededor del cuadro delimitador. |
| [TOP_BOTTOM](#TOP-BOTTOM) | El texto se detiene en la parte superior de la forma y se reinicia en la línea debajo de la forma. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


La forma permanece en la misma capa que el texto y se trata como un carácter.

### NONE {#NONE}
```
public static int NONE
```


Sin ajuste de texto alrededor de la forma. La forma se coloca detrás o delante del texto.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Ajusta el texto alrededor de todos los lados del cuadro delimitador cuadrado de la forma.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Igual que Tight, pero ajusta dentro de cualquier parte de la forma que esté abierta.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Ajusta estrechamente alrededor de los bordes de la forma, en lugar de ajustarse alrededor del cuadro delimitador.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


El texto se detiene en la parte superior de la forma y se reinicia en la línea debajo de la forma.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
