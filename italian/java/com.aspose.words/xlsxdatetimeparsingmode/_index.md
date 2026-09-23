---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come il testo del documento viene analizzato per identificare valori di data e ora in Java."
type: docs
weight: 742
url: /it/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Specifica come il testo del documento viene analizzato per identificare valori di data e ora.

 **Examples:** 

Mostra come specificare il rilevamento automatico del formato data e ora.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Il formato data/ora utilizzato in un documento viene determinato automaticamente. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | Il formato data/ora impostato per il thread corrente viene utilizzato per primo per analizzare i valori stringa. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Il formato data/ora utilizzato in un documento viene determinato automaticamente. Questo può richiedere tempo aggiuntivo.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


Il formato data/ora impostato per il thread corrente viene utilizzato per primo per analizzare i valori stringa. Se l'analisi fallisce, vengono provati altri formati data/ora comuni.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
