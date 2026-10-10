---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words per Java"
description: "Specifica le opzioni per il metodo MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions in Java."
type: docs
weight: 381
url: /it/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

Specifica le opzioni per il metodo **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**.

 **Examples:** 

Mostra come consentire una migliore conservazione dei bordi e dei margini visualizzati.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [NONE](#NONE) | Usa le opzioni predefinite quando inserisci HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Conserva le proprietà degli elementi a livello di blocco. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Rimuovi il paragrafo vuoto che viene normalmente inserito dopo l'HTML che termina con un elemento a livello di blocco. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Usa la formattazione di carattere e di paragrafo specificata in [DocumentBuilder](../../com.aspose.words/documentbuilder/) come formattazione di base per il testo inserito dall'HTML. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Usa le opzioni predefinite quando inserisci HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Conserva le proprietà degli elementi a livello di blocco.

 **Remarks:** 

Per impostazione predefinita, le proprietà dei blocchi genitore vengono unite e memorizzate nei loro elementi figlio (cioè paragrafi o tabelle). Se questa opzione è specificata, le proprietà di ogni blocco vengono memorizzate separatamente in una struttura logica speciale. Di conseguenza, questa opzione consente di conservare meglio i bordi e i margini individuali visualizzati nel documento HTML e ottenere risultati di conversione migliori. L'aspetto negativo è che il documento risultante diventa più difficile da modificare, poiché i bordi e i margini memorizzati nella struttura logica non sono disponibili per la modifica.

Vengono conservati solo i margini e i bordi degli elementi HTML 'body', 'div' e 'blockquote'. Le proprietà di ciascun elemento HTML vengono memorizzate separatamente.

Se questa opzione è specificata, Aspose.Words imita il comportamento di MS Word per quanto riguarda l'importazione delle proprietà dei blocchi.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Rimuovi il paragrafo vuoto che viene normalmente inserito dopo l'HTML che termina con un elemento a livello di blocco.

 **Remarks:** 

Per impostazione predefinita, [DocumentBuilder](../../com.aspose.words/documentbuilder/) garantisce che l'ultimo elemento a livello di blocco importato dall'HTML venga chiuso dopo l'importazione e inserisce un'interruzione di paragrafo dopo l'elemento. Questa interruzione di paragrafo separa il contenuto importato dall'HTML dal contenuto del documento modello. Tuttavia, se un frammento HTML viene inserito in un paragrafo vuoto, tale interruzione di paragrafo creerà un paragrafo vuoto aggiuntivo. Se questo comportamento è indesiderato, specifica questa opzione.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Usa la formattazione di carattere e di paragrafo specificata in [DocumentBuilder](../../com.aspose.words/documentbuilder/) come formattazione di base per il testo inserito dall'HTML.

 **Remarks:** 

Se questa opzione non è specificata, la formattazione di [DocumentBuilder](../../com.aspose.words/documentbuilder/) viene ignorata e il testo viene inserito con la formattazione HTML predefinita. Di conseguenza, il testo appare come viene visualizzato nei browser.

Se questa opzione è specificata, la formattazione del testo inserito si basa sulla formattazione specificata in [DocumentBuilder](../../com.aspose.words/documentbuilder/), e il testo appare come se fosse stato inserito usando [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
