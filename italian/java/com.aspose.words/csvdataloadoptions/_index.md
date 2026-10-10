---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words per Java"
description: "Rappresenta le opzioni per l'analisi dei dati CSV in Java."
type: docs
weight: 137
url: /it/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Rappresenta le opzioni per l'analisi dei dati CSV.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Un'istanza di questa classe può essere passata ai costruttori di [CsvDataSource](../../com.aspose.words/csvdatasource/).

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Inizializza una nuova istanza di questa classe con le opzioni predefinite. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Inizializza una nuova istanza di questa classe specificando se i dati CSV contengono i nomi delle colonne nella prima riga. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Restituisce il carattere utilizzato per commentare le righe dei dati CSV. |
| [getDelimiter()](#getDelimiter) | Restituisce il carattere da utilizzare come delimitatore di colonna. |
| [getQuoteChar()](#getQuoteChar) | Restituisce il carattere utilizzato per racchiudere i valori dei campi. |
| [hasHeaders()](#hasHeaders) | Restituisce un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Imposta un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne. |
| [setCommentChar(char value)](#setCommentChar-char) | Imposta il carattere utilizzato per commentare le righe dei dati CSV. |
| [setDelimiter(char value)](#setDelimiter-char) | Imposta il carattere da utilizzare come delimitatore di colonna. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Imposta il carattere utilizzato per racchiudere i valori dei campi. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Inizializza una nuova istanza di questa classe con le opzioni predefinite.

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Inizializza una nuova istanza di questa classe specificando se i dati CSV contengono i nomi delle colonne nella prima riga.

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Restituisce il carattere utilizzato per commentare le righe dei dati CSV.

 **Remarks:** 

Il valore predefinito è '\\#' (cancelletto).

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Il carattere utilizzato per commentare le righe di dati CSV.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Restituisce il carattere da utilizzare come delimitatore di colonna.

 **Remarks:** 

Il valore predefinito è ',' (virgola).

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Il carattere da utilizzare come delimitatore di colonna.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Restituisce il carattere utilizzato per racchiudere i valori dei campi.

 **Remarks:** 

Il valore predefinito è '\"' (virgoletta).

Raddoppia il carattere per inserirlo in testo tra virgolette.

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
char - Il carattere utilizzato per racchiudere tra virgolette i valori dei campi.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Restituisce un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Returns:**
boolean - Un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Imposta un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che indica se il primo record dei dati CSV contiene i nomi delle colonne. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Imposta il carattere utilizzato per commentare le righe dei dati CSV.

 **Remarks:** 

Il valore predefinito è '\\#' (cancelletto).

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | char | Il carattere utilizzato per commentare le righe di dati CSV. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Imposta il carattere da utilizzare come delimitatore di colonna.

 **Remarks:** 

Il valore predefinito è ',' (virgola).

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | char | Il carattere da utilizzare come delimitatore di colonna. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Imposta il carattere utilizzato per racchiudere i valori dei campi.

 **Remarks:** 

Il valore predefinito è '\"' (virgoletta).

Raddoppia il carattere per inserirlo in testo tra virgolette.

 **Examples:** 

Mostra come utilizzare CSV come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | char | Il carattere utilizzato per racchiudere tra virgolette i valori dei campi. |

