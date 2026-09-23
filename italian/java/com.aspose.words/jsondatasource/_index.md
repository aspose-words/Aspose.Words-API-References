---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso ai dati di un file JSON o di uno stream da utilizzare all'interno di un report in Java."
type: docs
weight: 409
url: /it/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Fornisce l'accesso ai dati di un file JSON o di uno stream da utilizzare all'interno di un report.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Per accedere ai dati del file o stream corrispondente durante la generazione di un report, passa un'istanza di questa classe come origine dati a una delle [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport sovraccarichi.

Nei documenti modello, se un elemento JSON di livello superiore è un array, un'istanza di [JsonDataSource](../../com.aspose.words/jsondatasource/) dovrebbe essere trattata allo stesso modo di un'istanza di [DataTable](../../com.aspose.words.net.system.data/datatable/). Se un elemento JSON di livello superiore è un oggetto, un'istanza di [JsonDataSource](../../com.aspose.words/jsondatasource/) dovrebbe essere trattata allo stesso modo di un'istanza di [DataRow](../../com.aspose.words.net.system.data/datarow/). Per ulteriori informazioni, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Nei documenti modello, è possibile lavorare con valori tipizzati degli elementi JSON. Per comodità, il motore sostituisce l'insieme dei tipi semplici JSON con il seguente:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Il motore riconosce automaticamente i valori dei tipi aggiuntivi in base alle loro rappresentazioni JSON.

Per sovrascrivere il comportamento predefinito del caricamento dei dati JSON, inizializza e passa un'istanza di [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) al costruttore di questa classe.

 **Examples:** 

Mostra come utilizzare JSON come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Inizializza una nuova istanza di questa classe. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni specificate per l'analisi dei dati JSON. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Inizializza una nuova istanza di questa classe. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni predefinite per l'analisi dei dati JSON.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonPath | java.lang.String | Il percorso del file JSON da utilizzare come origine dati. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


Crea una nuova origine dati con i dati di un file JSON utilizzando le opzioni specificate per l'analisi dei dati JSON.

 **Examples:** 

Mostra come utilizzare JSON come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonPath | java.lang.String | Il percorso del file JSON da utilizzare come origine dati. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | Opzioni per l'analisi dei dati JSON. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

