---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words para Java"
description: "Especifica a qué es relativa la posición vertical de una forma o marco de texto en Java."
type: docs
weight: 563
url: /es/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Especifica a qué es relativa la posición vertical de una forma o marco de texto.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Especifica que la posición vertical debe ser relativa al margen inferior de la página actual. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Especifica que la posición vertical debe ser relativa al margen interior de la página actual. |
| [LINE](#LINE) | Sin documentación. |
| [MARGIN](#MARGIN) | Especifica que la posición vertical debe ser relativa a los márgenes de la página. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Especifica que la posición vertical debe ser relativa al margen exterior de la página actual. |
| [PAGE](#PAGE) | El objeto está posicionado relativo al borde superior de la página. |
| [PARAGRAPH](#PARAGRAPH) | El objeto está posicionado relativo a la parte superior del párrafo que contiene la ancla. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | El valor predeterminado es [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | El valor predeterminado es [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Especifica que la posición vertical debe ser relativa al margen superior de la página actual. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Especifica que la posición vertical debe ser relativa al margen inferior de la página actual.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Especifica que la posición vertical debe ser relativa al margen interior de la página actual.

### LINE {#LINE}
```
public static int LINE
```


Sin documentación.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Especifica que la posición vertical debe ser relativa a los márgenes de la página.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Especifica que la posición vertical debe ser relativa al margen exterior de la página actual.

### PAGE {#PAGE}
```
public static int PAGE
```


El objeto está posicionado relativo al borde superior de la página.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


El objeto está posicionado relativo a la parte superior del párrafo que contiene la ancla.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


El valor predeterminado es [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


El valor predeterminado es [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Especifica que la posición vertical debe ser relativa al margen superior de la página actual.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
