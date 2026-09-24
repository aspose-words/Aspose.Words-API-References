---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words para Java"
description: "Especifica a qué es relativa la posición horizontal de una forma o marco de texto en Java."
type: docs
weight: 561
url: /es/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Especifica a qué es relativa la posición horizontal de una forma o marco de texto.

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
| [CHARACTER](#CHARACTER) | El objeto se posiciona relativo al lado izquierdo del párrafo. |
| [COLUMN](#COLUMN) | El objeto se posiciona relativo al lado izquierdo de la columna. |
| [DEFAULT](#DEFAULT) | El valor predeterminado es [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Especifica que la posición horizontal debe ser relativa al margen interior de la página actual (el margen izquierdo en páginas impares, el derecho en páginas pares). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Especifica que la posición horizontal debe ser relativa al margen izquierdo de la página. |
| [MARGIN](#MARGIN) | Especifica que la posición horizontal debe ser relativa a los márgenes de la página. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Especifica que la posición horizontal debe ser relativa al margen exterior de la página actual (el margen derecho en páginas impares, el izquierdo en páginas pares). |
| [PAGE](#PAGE) | El objeto se posiciona relativo al borde izquierdo de la página. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Especifica que la posición horizontal debe ser relativa al margen derecho de la página. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


El objeto se posiciona relativo al lado izquierdo del párrafo.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


El objeto se posiciona relativo al lado izquierdo de la columna.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


El valor predeterminado es [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Especifica que la posición horizontal debe ser relativa al margen interior de la página actual (el margen izquierdo en páginas impares, el derecho en páginas pares).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Especifica que la posición horizontal debe ser relativa al margen izquierdo de la página.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Especifica que la posición horizontal debe ser relativa a los márgenes de la página.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Especifica que la posición horizontal debe ser relativa al margen exterior de la página actual (el margen derecho en páginas impares, el izquierdo en páginas pares).

### PAGE {#PAGE}
```
public static int PAGE
```


El objeto se posiciona relativo al borde izquierdo de la página.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Especifica que la posición horizontal debe ser relativa al margen derecho de la página.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
