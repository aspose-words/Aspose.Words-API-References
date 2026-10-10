---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words per Java"
description: "Valori possibili per la modalità di visualizzazione in Microsoft Word in Java."
type: docs
weight: 715
url: /it/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Valori possibili per la modalità di visualizzazione in Microsoft Word.

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
| [NONE](#NONE) | Il documento deve essere visualizzato nella vista predefinita dell'applicazione. |
| [NORMAL](#NORMAL) | Il documento deve essere visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi. |
| [OUTLINE](#OUTLINE) | Il documento deve essere visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | Il documento deve essere aperto in una vista che mostra il documento così come verrà stampato. |
| [READING](#READING) | Il documento deve essere visualizzato nella vista predefinita dell'applicazione. |
| [WEB](#WEB) | Il documento deve essere visualizzato in una vista che imita il modo in cui questo documento verrebbe mostrato in una pagina web. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Il documento deve essere visualizzato nella vista predefinita dell'applicazione.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Il documento deve essere visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Il documento deve essere visualizzato in una vista ottimizzata per la creazione di schemi o di documenti lunghi.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


Il documento deve essere aperto in una vista che mostra il documento così come verrà stampato.

### READING {#READING}
```
public static int READING
```


Il documento deve essere visualizzato nella vista predefinita dell'applicazione.

### WEB {#WEB}
```
public static int WEB
```


Il documento deve essere visualizzato in una vista che imita il modo in cui questo documento verrebbe mostrato in una pagina web.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
