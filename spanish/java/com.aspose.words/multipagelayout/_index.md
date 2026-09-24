---
title: "MultiPageLayout"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words para Java"
description: "Define un diseño para renderizar múltiples páginas en una única salida en Java."
type: docs
weight: 472
url: /es/java/com.aspose.words/multipagelayout/
---

**Inheritance:**
java.lang.Object
```
public class MultiPageLayout
```

Define un diseño para renderizar múltiples páginas en una única salida.

 **Remarks:** 

Utilice uno de los métodos de fábrica estáticos para crear una configuración de diseño.

 **Examples:** 

Muestra cómo guardar el documento en una imagen JPG con la configuración de diseño multipágina.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set up a grid layout with:
 // - 3 columns per row.
 // - 10pts spacing between pages (horizontal and vertical).
 options.setPageLayout(MultiPageLayout.grid(3, 10f, 10f));

 // Alternative layouts:
 // options.PageLayout = MultiPageLayout.Horizontal(10);
 // options.PageLayout = MultiPageLayout.Vertical(10);

 // Customize the background and border.
 options.getPageLayout().setBackColor(Color.lightGray);
 options.getPageLayout().setBorderColor(Color.BLUE);
 options.getPageLayout().setBorderWidth(2f);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GridLayout.jpg", options);
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getBackColor()](#getBackColor) | Obtiene el color de fondo de la salida. |
| [getBorderColor()](#getBorderColor) | Obtiene el color del borde de las páginas. |
| [getBorderWidth()](#getBorderWidth) | Obtiene el ancho del borde de las páginas. |
| [grid(int columns, float horizontalGap, float verticalGap)](#grid-int-float-float) | Crea un diseño en el que las páginas se renderizan de izquierda a derecha, de arriba a abajo, en una cuadrícula con el número especificado de columnas. |
| [horizontal(float horizontalGap)](#horizontal-float) | Crea un diseño en el que todas las páginas especificadas se renderizan horizontalmente una al lado de la otra, de izquierda a derecha, en una única salida. |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Establece el color de fondo de la salida. |
| [setBorderColor(Color value)](#setBorderColor-java.awt.Color) | Establece el color del borde de las páginas. |
| [setBorderWidth(float value)](#setBorderWidth-float) | Establece el ancho del borde de las páginas. |
| [singlePage()](#singlePage) | Crea un diseño que renderiza solo la primera de las páginas especificadas. |
| [tiffFrames()](#tiffFrames) | Crea un diseño donde cada página se renderiza como un marco separado en una imagen TIFF multi-marco. |
| [vertical(float verticalGap)](#vertical-float) | Crea un diseño donde todas las páginas especificadas se renderizan verticalmente una debajo de la otra en una única salida. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Obtiene el color de fondo de la salida. El valor predeterminado es java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - El color de fondo de la salida.
### getBorderColor() {#getBorderColor}
```
public Color getBorderColor()
```


Obtiene el color del borde de las páginas. El valor predeterminado es java.awt.Color\#EMPTY.EMPTY.

**Returns:**
java.awt.Color - El color del borde de las páginas.
### getBorderWidth() {#getBorderWidth}
```
public float getBorderWidth()
```


Obtiene el ancho del borde de la página. El valor predeterminado es 0.

**Returns:**
float - El ancho del borde de la página.
### grid(int columns, float horizontalGap, float verticalGap) {#grid-int-float-float}
```
public static MultiPageLayout grid(int columns, float horizontalGap, float verticalGap)
```


Crea un diseño en el que las páginas se renderizan de izquierda a derecha, de arriba a abajo, en una cuadrícula con el número especificado de columnas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnas | int | El número de columnas en el diseño. Debe ser mayor que cero. |
| horizontalGap | float | El espacio horizontal entre columnas en puntos. |
| verticalGap | float | El espacio vertical entre filas en puntos. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### horizontal(float horizontalGap) {#horizontal-float}
```
public static MultiPageLayout horizontal(float horizontalGap)
```


Crea un diseño en el que todas las páginas especificadas se renderizan horizontalmente una al lado de la otra, de izquierda a derecha, en una única salida.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| horizontalGap | float | El espacio horizontal entre páginas en puntos. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


Establece el color de fondo de la salida. El valor predeterminado es java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color de fondo de la salida. |

### setBorderColor(Color value) {#setBorderColor-java.awt.Color}
```
public void setBorderColor(Color value)
```


Establece el color del borde de la página. El valor predeterminado es java.awt.Color\#EMPTY.EMPTY.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.awt.Color | El color del borde de la página. |

### setBorderWidth(float value) {#setBorderWidth-float}
```
public void setBorderWidth(float value)
```


Establece el ancho del borde de la página. El valor predeterminado es 0.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | float | El ancho del borde de la página. |

### singlePage() {#singlePage}
```
public static MultiPageLayout singlePage()
```


Crea un diseño que renderiza solo la primera de las páginas especificadas.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### tiffFrames() {#tiffFrames}
```
public static MultiPageLayout tiffFrames()
```


Crea un diseño donde cada página se renderiza como un marco separado en una imagen TIFF de varios marcos. Aplicable solo a formatos de imagen TIFF.

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
### vertical(float verticalGap) {#vertical-float}
```
public static MultiPageLayout vertical(float verticalGap)
```


Crea un diseño donde todas las páginas especificadas se renderizan verticalmente una debajo de la otra en una única salida.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| verticalGap | float | El espacio vertical entre páginas en puntos. |

**Returns:**
[MultiPageLayout](../../com.aspose.words/multipagelayout/)
