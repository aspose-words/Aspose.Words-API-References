---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words para Java"
description: "Valores posibles para el modo de vista en Microsoft Word en Java."
type: docs
weight: 715
url: /es/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Valores posibles para el modo de vista en Microsoft Word.

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
| [NONE](#NONE) | El documento se renderizará en la vista predeterminada de la aplicación. |
| [NORMAL](#NORMAL) | El documento se renderizará en una vista optimizada para esquematizar o crear documentos extensos. |
| [OUTLINE](#OUTLINE) | El documento se renderizará en una vista optimizada para esquematizar o crear documentos extensos. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | El documento se abrirá en una vista que muestra el documento tal como se imprimirá. |
| [READING](#READING) | El documento se renderizará en la vista predeterminada de la aplicación. |
| [WEB](#WEB) | El documento se renderizará en una vista que imita la forma en que este documento se mostraría en una página web. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


El documento se renderizará en la vista predeterminada de la aplicación.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


El documento se renderizará en una vista optimizada para esquematizar o crear documentos extensos.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


El documento se renderizará en una vista optimizada para esquematizar o crear documentos extensos.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


El documento se abrirá en una vista que muestra el documento tal como se imprimirá.

### READING {#READING}
```
public static int READING
```


El documento se renderizará en la vista predeterminada de la aplicación.

### WEB {#WEB}
```
public static int WEB
```


El documento se renderizará en una vista que imita la forma en que este documento se mostraría en una página web.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
