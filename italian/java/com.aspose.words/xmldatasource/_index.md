---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso ai dati di un file XML o di uno stream da utilizzare all'interno di un report in Java."
type: docs
weight: 746
url: /it/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Fornisce l'accesso ai dati di un file o flusso XML da utilizzare all'interno di un report.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Per accedere ai dati del file o stream corrispondente durante la generazione di un report, passa un'istanza di questa classe come origine dati a una delle [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport sovraccarichi.

Nei documenti modello, se un elemento XML di livello superiore contiene solo un elenco di elementi dello stesso tipo, un'istanza di [XmlDataSource](../../com.aspose.words/xmldatasource/) dovrebbe essere trattata allo stesso modo di un'istanza di [DataTable](../../com.aspose.words.net.system.data/datatable/). Altrimenti, un'istanza di [XmlDataSource](../../com.aspose.words/xmldatasource/) dovrebbe essere trattata allo stesso modo di un'istanza di [DataRow](../../com.aspose.words.net.system.data/datarow/). Per ulteriori informazioni, consultare il riferimento della sintassi del modello (https://docs.aspose.com/display/wordsjava/Template+Syntax).

Quando la definizione XML Schema viene passata al costruttore di questa classe, i tipi di dati dei valori di elementi XML semplici e attributi sono determinati in base allo schema. Pertanto, nei documenti modello, è possibile lavorare con valori tipizzati anziché solo con stringhe.

Quando la definizione XML Schema non viene passata al costruttore di questa classe, i tipi di dati dei valori di elementi XML semplici e attributi sono determinati automaticamente in base alle loro rappresentazioni stringa. Pertanto, nei documenti modello, è possibile lavorare con valori tipizzati anche in questo caso. Il motore è in grado di riconoscere automaticamente i valori dei seguenti tipi:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Nota che per far funzionare il riconoscimento automatico dei tipi di dati, le rappresentazioni stringa dei valori di elementi XML semplici e attributi devono essere generate utilizzando impostazioni culturali invarianti.

Per sovrascrivere il comportamento predefinito del caricamento dei dati XML, inizializza e passa un'istanza di [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) al costruttore di questa classe.

 **Examples:** 

Mostra come utilizzare XML come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

Mostra come utilizzare XML come origine dati (stream).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Crea una nuova origine dati con i dati provenienti da un file XML utilizzando le opzioni predefinite per il caricamento dei dati XML. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Inizializza una nuova istanza di questa classe. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Crea una nuova origine dati con i dati provenienti da un file XML utilizzando un file XML Schema Definition. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Inizializza una nuova istanza di questa classe. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crea una nuova origine dati con i dati provenienti da un file XML utilizzando le opzioni specificate per il caricamento dei dati XML. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Inizializza una nuova istanza di questa classe. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crea una nuova origine dati con i dati provenienti da un file XML utilizzando un file XML Schema Definition. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Inizializza una nuova istanza di questa classe. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Crea una nuova origine dati con i dati provenienti da un file XML utilizzando le opzioni predefinite per il caricamento dei dati XML.

 **Examples:** 

Mostra come utilizzare XML come origine dati (stringa).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | java.lang.String | Il percorso del file XML da utilizzare come origine dati. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Crea una nuova origine dati con i dati provenienti da un file XML utilizzando un file XML Schema Definition. Vengono utilizzate le opzioni predefinite per il caricamento dei dati XML.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | java.lang.String | Il percorso del file XML da utilizzare come origine dati. |
| xmlSchemaPath | java.lang.String | Il percorso del file XML Schema Definition che fornisce lo schema per il file XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Crea una nuova origine dati con i dati provenienti da un file XML utilizzando le opzioni specificate per il caricamento dei dati XML.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | java.lang.String | Il percorso del file XML da utilizzare come origine dati. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Opzioni per il caricamento dei dati XML. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Crea una nuova origine dati con i dati provenienti da un file XML utilizzando un file XML Schema Definition. Le opzioni specificate sono utilizzate per il caricamento dei dati XML.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | java.lang.String | Il percorso del file XML da utilizzare come origine dati. |
| xmlSchemaPath | java.lang.String | Il percorso del file XML Schema Definition che fornisce lo schema per il file XML. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Opzioni per il caricamento dei dati XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Inizializza una nuova istanza di questa classe.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

