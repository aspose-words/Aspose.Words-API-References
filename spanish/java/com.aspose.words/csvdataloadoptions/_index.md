---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words para Java"
description: "Representa opciones para analizar datos CSV en Java."
type: docs
weight: 137
url: /es/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

Representa opciones para analizar datos CSV.

Para obtener más información, visite el artículo de documentación [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Una instancia de esta clase puede pasarse a los constructores de [CsvDataSource](../../com.aspose.words/csvdatasource/).

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Inicializa una nueva instancia de esta clase con opciones predeterminadas. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Inicializa una nueva instancia de esta clase especificando si los datos CSV contienen nombres de columna en la primera línea. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getCommentChar()](#getCommentChar) | Obtiene el carácter que se usa para comentar líneas de datos CSV. |
| [getDelimiter()](#getDelimiter) | Obtiene el carácter que se usará como delimitador de columnas. |
| [getQuoteChar()](#getQuoteChar) | Obtiene el carácter que se usa para citar valores de campo. |
| [hasHeaders()](#hasHeaders) | Obtiene un valor que indica si el primer registro de datos CSV contiene nombres de columna. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | Establece un valor que indica si el primer registro de datos CSV contiene nombres de columna. |
| [setCommentChar(char value)](#setCommentChar-char) | Establece el carácter que se usa para comentar líneas de datos CSV. |
| [setDelimiter(char value)](#setDelimiter-char) | Establece el carácter que se usará como delimitador de columnas. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Establece el carácter que se usa para citar valores de campo. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Inicializa una nueva instancia de esta clase con opciones predeterminadas.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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


Inicializa una nueva instancia de esta clase especificando si los datos CSV contienen nombres de columna en la primera línea.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


Obtiene el carácter que se usa para comentar líneas de datos CSV.

 **Remarks:** 

El valor predeterminado es '\#' (signo de número).

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
char - El carácter que se usa para comentar líneas de datos CSV.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Obtiene el carácter que se usará como delimitador de columnas.

 **Remarks:** 

El valor predeterminado es ',' (coma).

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
char - El carácter que se usará como delimitador de columnas.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Obtiene el carácter que se usa para citar valores de campo.

 **Remarks:** 

El valor predeterminado es '\"' (comilla).

Duplica el carácter para insertarlo en texto entre comillas.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
char - El carácter que se usa para citar valores de campo.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


Obtiene un valor que indica si el primer registro de datos CSV contiene nombres de columna.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
boolean - Un valor que indica si el primer registro de datos CSV contiene nombres de columnas.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


Establece un valor que indica si el primer registro de datos CSV contiene nombres de columna.

 **Remarks:** 

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si el primer registro de datos CSV contiene nombres de columnas. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


Establece el carácter que se usa para comentar líneas de datos CSV.

 **Remarks:** 

El valor predeterminado es '\#' (signo de número).

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | El carácter que se usa para comentar líneas de datos CSV. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Establece el carácter que se usará como delimitador de columnas.

 **Remarks:** 

El valor predeterminado es ',' (coma).

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | El carácter que se usará como delimitador de columnas. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Establece el carácter que se usa para citar valores de campo.

 **Remarks:** 

El valor predeterminado es '\"' (comilla).

Duplica el carácter para insertarlo en texto entre comillas.

 **Examples:** 

Muestra cómo usar CSV como fuente de datos (cadena).

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | El carácter que se usa para citar valores de campo. |

