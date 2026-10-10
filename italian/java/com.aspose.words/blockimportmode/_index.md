---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words per Java"
description: "Specifica come le proprietà degli elementi a livello di blocco vengono importate dai documenti basati su HTML in Java."
type: docs
weight: 39
url: /it/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Specifica come le proprietà degli elementi a livello di blocco vengono importate dai documenti basati su HTML.

 **Examples:** 

Mostra come le proprietà degli elementi a livello di blocco vengono importate dai documenti basati su HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [MERGE](#MERGE) | Le proprietà dei blocchi genitore vengono unite e memorizzate sugli elementi figlio (ad es. |
| [PRESERVE](#PRESERVE) | Le proprietà dei blocchi genitore vengono importate in una struttura logica speciale e sono memorizzate separatamente dai nodi del documento. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Le proprietà dei blocchi genitore vengono unite e memorizzate sugli elementi figlio (ad es. paragrafi o tabelle).

 **Remarks:** 

Le proprietà dei blocchi genitore vengono unite come segue: i margini vengono sommati; i bordi dei blocchi di livello superiore vengono scartati e vengono conservati solo i bordi del livello più interno. Di conseguenza, quando questa modalità è specificata, parte della formattazione dei blocchi del documento originale verrà persa.

D'altra parte, poiché tutte le proprietà dei blocchi a livello di blocco unite sono memorizzate sui nodi del documento, tutta la formattazione nel documento risultante sarà disponibile per la modifica.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Le proprietà dei blocchi genitore vengono importate in una struttura logica speciale e sono memorizzate separatamente dai nodi del documento.

 **Remarks:** 

Solo i margini e i bordi degli elementi HTML 'body', 'div' e 'blockquote' vengono importati. Le proprietà di ciascun elemento HTML sono memorizzate singolarmente.

Questa modalità consente di preservare meglio i bordi e i margini presenti nel documento HTML e di ottenere risultati di conversione migliori. L'aspetto negativo è che il documento risultante diventa più difficile da modificare, poiché i bordi e i margini memorizzati nella struttura logica non sono disponibili per la modifica.

Questa modalità imita il comportamento di MS Word per quanto riguarda l'importazione delle proprietà dei blocchi.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
