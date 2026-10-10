---
title: "ReportBuildOptions"
linktitle: "ReportBuildOptions"
second_title: "Aspose.Words per Java"
description: "Specifica le opzioni che controllano il comportamento di ReportingEngine durante la generazione di un report in Java."
type: docs
weight: 570
url: /it/java/com.aspose.words/reportbuildoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuildOptions
```

Specifica le opzioni che controllano il comportamento di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report.
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Specifica che i membri mancanti dell'oggetto devono essere trattati come letterali null dal motore. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Specifica che il motore deve inserire inline i messaggi di errore della sintassi del modello nei documenti di output. |
| [NONE](#NONE) | Specifica le opzioni predefinite. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Specifica che il motore deve rimuovere i paragrafi che diventano vuoti dopo che i tag di sintassi del modello sono stati rimossi o sostituiti con valori vuoti. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) | Specifica che il motore deve utilizzare i valori di orientamento immagine EXIF \\u200b\\u200bimage per ruotare correttamente le immagini JPEG inserite. |
| [UPDATE_FIELDS_SYNTAX_AWARE](#UPDATE-FIELDS-SYNTAX-AWARE) | Specifica che il motore deve ignorare la sintassi del modello nei risultati dei campi e aggiornare i campi dopo la generazione di un report. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Specifica che il motore deve visitare i nodi figlio della sezione (intestazioni, piè di pagina, corpi) in un ordine compatibile con le versioni di Aspose.Words precedenti la 21.9. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int reportBuildOptions)](#getName-int) |  |
| [getNames(int reportBuildOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int reportBuildOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Specifica che i membri mancanti dell'oggetto devono essere trattati come letterali null dal motore. Questa opzione influisce solo sull'accesso ai membri di istanza (cioè non statici) e ai metodi di estensione. Se questa opzione non è impostata, il motore genera un'eccezione quando incontra un membro mancante dell'oggetto.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Specifica che il motore deve inserire inline i messaggi di errore di sintassi del modello nei documenti di output. Se questa opzione non è impostata, il motore genera un'eccezione quando incontra un errore di sintassi.

### NONE {#NONE}
```
public static int NONE
```


Specifica le opzioni predefinite.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Specifica che il motore deve rimuovere i paragrafi che diventano vuoti dopo che i tag di sintassi del modello sono stati rimossi o sostituiti con valori vuoti.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


Specifica che il motore deve utilizzare i valori di orientamento immagine EXIF \\u200b\\u200bimage per ruotare correttamente le immagini JPEG inserite.

### UPDATE_FIELDS_SYNTAX_AWARE {#UPDATE-FIELDS-SYNTAX-AWARE}
```
public static int UPDATE_FIELDS_SYNTAX_AWARE
```


Specifica che il motore deve ignorare la sintassi del modello nei risultati dei campi e aggiornare i campi dopo la generazione di un report.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Specifica che il motore deve visitare i nodi figlio della sezione (intestazioni, piè di pagina, corpi) in un ordine compatibile con le versioni di Aspose.Words precedenti la 21.9.

 **Remarks:** 

Per impostazione predefinita, il motore tratta le intestazioni e i piè di pagina come se fossero collegati alle interruzioni di sezione. Cioè, durante la visita dei nodi figlio della sezione, il corpo viene visitato per primo e solo successivamente vengono visitate le intestazioni e i piè di pagina. Questo è coerente con il comportamento di Microsoft Word durante il copia-incolla o la rimozione di contenuti multi-sezione e produce risultati più corretti nella maggior parte degli scenari.

Prima di Aspose.Words 21.9, il motore utilizzava un altro ordine di visita: i nodi figlio della sezione venivano visitati nell'ordine in cui appaiono nel documento. Applica questo valore a [ReportingEngine.getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) se è necessaria la compatibilità con versioni precedenti di Aspose.Words.

### length {#length}
```
public static int length
```


### fromName(String reportBuildOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String reportBuildOptionsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int reportBuildOptions) {#getName-int}
```
public static String getName(int reportBuildOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int}
```
public static Set getNames(int reportBuildOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int reportBuildOptions) {#toString-int}
```
public static String toString(int reportBuildOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
