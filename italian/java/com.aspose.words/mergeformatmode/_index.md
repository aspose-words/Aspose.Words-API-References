---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words per Java"
description: "Specifica come la formattazione viene unita quando si combinano più documenti in Java."
type: docs
weight: 464
url: /it/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

Specifica come la formattazione viene unita quando si combinano più documenti.

 **Examples:** 

Mostra come unire i documenti in un unico documento di output.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Significa che il documento di origine manterrà la sua formattazione originale, come stili di carattere, dimensioni, colori, rientri e qualsiasi altro elemento di formattazione applicato al suo contenuto. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | Preserva il layout dei documenti originali nel documento finale. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | Combina la formattazione dei documenti uniti. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Significa che il documento di origine manterrà la sua formattazione originale, come stili di carattere, dimensioni, colori, rientri e qualsiasi altro elemento di formattazione applicato al suo contenuto.

 **Remarks:** 

Utilizzando questa opzione, ti assicuri che il contenuto copiato appaia come nel documento originale, indipendentemente dalle impostazioni di formattazione del primo documento nella coda di unione.

Questa opzione non ha alcun effetto quando i formati di input e output sono PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


Preserva il layout dei documenti originali nel documento finale.

 **Remarks:** 

In generale, sembra che tu stampi i documenti originali e li incolli manualmente insieme usando della colla.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


Combina la formattazione dei documenti uniti.

 **Remarks:** 

Utilizzando questa opzione, Aspose.Words adatta la formattazione del primo documento per corrispondere alla struttura e all'aspetto del secondo documento, ma mantiene intatta parte della formattazione originale. Questa opzione è utile quando desideri mantenere l'aspetto generale del documento di destinazione ma conservare comunque alcuni aspetti della formattazione del documento originale.

Questa opzione non ha alcun effetto quando i formati di input e output sono PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
