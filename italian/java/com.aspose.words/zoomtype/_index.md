---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words per Java"
description: "Valori possibili per la dimensione con cui il documento appare sullo schermo in Microsoft Word in Java."
type: docs
weight: 751
url: /it/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Valori possibili per la dimensione con cui il documento appare sullo schermo in Microsoft Word.

 **Examples:** 

Mostra come impostare un fattore di zoom personalizzato, che le versioni precedenti di Microsoft Word applicheranno a un documento al caricamento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CUSTOM](#CUSTOM) | La percentuale di zoom è impostata esplicitamente. |
| [FULL_PAGE](#FULL-PAGE) | La percentuale di zoom è ricalcolata automaticamente per adattarsi a una pagina intera. |
| [NONE](#NONE) | Indica di utilizzare la percentuale di zoom esplicita. |
| [PAGE_WIDTH](#PAGE-WIDTH) | La percentuale di zoom è ricalcolata automaticamente per adattarsi alla larghezza della pagina. |
| [TEXT_FIT](#TEXT-FIT) | La percentuale di zoom è ricalcolata automaticamente per adattarsi al testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


La percentuale di zoom è impostata esplicitamente. Non viene ricalcolata automaticamente quando le dimensioni del controllo cambiano.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


La percentuale di zoom è ricalcolata automaticamente per adattarsi a una pagina intera.

### NONE {#NONE}
```
public static int NONE
```


Indica di utilizzare la percentuale di zoom esplicita. Stesso di [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


La percentuale di zoom è ricalcolata automaticamente per adattarsi alla larghezza della pagina.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


La percentuale di zoom è ricalcolata automaticamente per adattarsi al testo.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
