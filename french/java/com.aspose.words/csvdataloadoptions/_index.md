---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words pour Java"
description: "Représente les options pour analyser les données CSV en Java."
type: docs
weight: 137
url: /fr/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Représente les options d'analyse des données CSV.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Une instance de cette classe peut être transmise aux constructeurs de [CsvDataSource](../../com.aspose.words/csvdatasource/).

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
## Constructors

| Constructor | Description |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Initialise une nouvelle instance de cette classe avec les options par défaut. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Initialise une nouvelle instance de cette classe en spécifiant si les données CSV contiennent des noms de colonnes à la première ligne. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Obtient le caractère utilisé pour commenter les lignes de données CSV. |
| [getDelimiter()](#getDelimiter) | Obtient le caractère à utiliser comme délimiteur de colonne. |
| [getQuoteChar()](#getQuoteChar) | Obtient le caractère utilisé pour entourer les valeurs de champ. |
| [hasHeaders()](#hasHeaders) | Obtient une valeur indiquant si le premier enregistrement des données CSV contient des noms de colonnes. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Définit une valeur indiquant si le premier enregistrement des données CSV contient des noms de colonnes. |
| [setCommentChar(char value)](#setCommentChar-char) | Définit le caractère utilisé pour commenter les lignes de données CSV. |
| [setDelimiter(char value)](#setDelimiter-char) | Définit le caractère à utiliser comme délimiteur de colonne. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Définit le caractère utilisé pour entourer les valeurs de champ. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Initialise une nouvelle instance de cette classe avec les options par défaut.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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


Initialise une nouvelle instance de cette classe en spécifiant si les données CSV contiennent des noms de colonnes à la première ligne.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
| Paramètre | Type | Description |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Obtient le caractère utilisé pour commenter les lignes de données CSV.

 **Remarks:** 

La valeur par défaut est '\\#' (signe dièse).

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
char - Le caractère utilisé pour commenter les lignes de données CSV.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Obtient le caractère à utiliser comme délimiteur de colonne.

 **Remarks:** 

La valeur par défaut est ',' (virgule).

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
char - Le caractère à utiliser comme délimiteur de colonne.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Obtient le caractère utilisé pour entourer les valeurs de champ.

 **Remarks:** 

La valeur par défaut est '\"' (guillemet).

Doublez le caractère pour le placer dans un texte entre guillemets.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
char - Le caractère utilisé pour encadrer les valeurs de champ.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Obtient une valeur indiquant si le premier enregistrement des données CSV contient des noms de colonnes.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
boolean - Une valeur indiquant si le premier enregistrement des données CSV contient les noms de colonnes.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Définit une valeur indiquant si le premier enregistrement des données CSV contient des noms de colonnes.

 **Remarks:** 

La valeur par défaut est false.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur indiquant si le premier enregistrement des données CSV contient les noms de colonnes. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Définit le caractère utilisé pour commenter les lignes de données CSV.

 **Remarks:** 

La valeur par défaut est '\\#' (signe dièse).

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | char | Le caractère utilisé pour commenter les lignes de données CSV. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Définit le caractère à utiliser comme délimiteur de colonne.

 **Remarks:** 

La valeur par défaut est ',' (virgule).

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | char | Le caractère à utiliser comme délimiteur de colonne. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Définit le caractère utilisé pour entourer les valeurs de champ.

 **Remarks:** 

La valeur par défaut est '\"' (guillemet).

Doublez le caractère pour le placer dans un texte entre guillemets.

 **Examples:** 

Montre comment utiliser le CSV comme source de données (chaîne).

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | char | Le caractère utilisé pour encadrer les valeurs de champ. |

