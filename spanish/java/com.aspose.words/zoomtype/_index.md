---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words para Java"
description: "Valores posibles para el tamaño con el que el documento aparece en la pantalla en Microsoft Word en Java."
type: docs
weight: 751
url: /es/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Valores posibles para el tamaño con el que el documento aparece en la pantalla en Microsoft Word.

 **Examples:** 

Muestra cómo establecer un factor de zoom personalizado, que las versiones anteriores de Microsoft Word aplicarán a un documento al cargarlo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CUSTOM](#CUSTOM) | El porcentaje de zoom se establece explícitamente. |
| [FULL_PAGE](#FULL-PAGE) | El porcentaje de zoom se recalcula automáticamente para ajustarse a una página completa. |
| [NONE](#NONE) | Indica que se use el porcentaje de zoom explícito. |
| [PAGE_WIDTH](#PAGE-WIDTH) | El porcentaje de zoom se recalcula automáticamente para ajustarse al ancho de la página. |
| [TEXT_FIT](#TEXT-FIT) | El porcentaje de zoom se recalcula automáticamente para ajustarse al texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


El porcentaje de zoom se establece explícitamente. No se recalcula automáticamente cuando cambia el tamaño del control.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


El porcentaje de zoom se recalcula automáticamente para ajustarse a una página completa.

### NONE {#NONE}
```
public static int NONE
```


Indica que se use el porcentaje de zoom explícito. Igual que [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


El porcentaje de zoom se recalcula automáticamente para ajustarse al ancho de la página.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


El porcentaje de zoom se recalcula automáticamente para ajustarse al texto.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
