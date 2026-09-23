---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso ai dati di un file CSV o di uno stream da utilizzare all'interno di un report in Java."
type: docs
weight: 138
url: /it/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Fornisce l'accesso ai dati di un file CSV o di uno stream da utilizzare all'interno di un report.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Per accedere ai dati del file o stream corrispondente durante la generazione di un report, passa un'istanza di questa classe come origine dati a una delle [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport sovraccarichi.

Nei documenti modello, un'istanza di [CsvDataSource](../../com.aspose.words/csvdatasource/) deve essere trattata allo stesso modo di un'istanza di [DataTable](../../com.aspose.words.net.system.data/datatable/). Per ulteriori informazioni, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsjava/Template+Syntax).

I tipi di dati dei valori separati da virgola vengono determinati automaticamente in base alle loro rappresentazioni stringa. Pertanto, nei documenti modello, è possibile lavorare con valori tipizzati anziché solo stringhe. Il motore è in grado di riconoscere automaticamente i valori dei seguenti tipi:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Nota che, per far funzionare il riconoscimento automatico dei tipi di dati, le rappresentazioni stringa dei valori separati da virgola devono essere formate utilizzando impostazioni culturali invarianti.

Per sovrascrivere il comportamento predefinito del caricamento dei dati CSV, inizializza e passa un'istanza di [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) al costruttore di questa classe.

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
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni specificate per l'analisi dei dati CSV. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Inizializza una nuova istanza di questa classe. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Inizializza una nuova istanza di questa classe. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvPath | java.lang.String | Il percorso del file CSV da utilizzare come origine dati. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


Crea una nuova origine dati con i dati di un file CSV utilizzando le opzioni specificate per l'analisi dei dati CSV.

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
| csvPath | java.lang.String | Il percorso del file CSV da utilizzare come origine dati. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | Opzioni per l'analisi dei dati CSV. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

