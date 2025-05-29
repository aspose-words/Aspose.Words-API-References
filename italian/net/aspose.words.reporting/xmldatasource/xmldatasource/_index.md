---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words per .NET
description: Crea senza sforzo una potente fonte di dati con il costruttore XmlDataSource, caricando i dati XML utilizzando opzioni predefinite ottimizzate per un'integrazione perfetta.
type: docs
weight: 10
url: /it/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Crea una nuova origine dati con dati da un file XML utilizzando le opzioni predefinite per il caricamento dei dati XML.

```csharp
public XmlDataSource(string xmlPath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | String | Percorso al file XML da utilizzare come origine dati. |

## Esempi

Mostra come utilizzare XML come origine dati (stringa).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Guarda anche

* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Crea una nuova origine dati con dati da un flusso XML utilizzando le opzioni predefinite per il caricamento dei dati XML.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | Stream | Flusso di dati XML da utilizzare come origine dati. |

## Esempi

Mostra come utilizzare XML come sorgente dati (flusso).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Guarda anche

* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Crea una nuova origine dati con dati da un file XML utilizzando un file XML Schema Definition. Le opzioni predefinite vengono utilizzate per il caricamento dei dati XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | String | Percorso al file XML da utilizzare come origine dati. |
| xmlSchemaPath | String | Percorso al file XML Schema Definition che fornisce lo schema per il file XML . |

### Guarda anche

* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Crea una nuova origine dati con dati provenienti da un flusso XML utilizzando un flusso XML Schema Definition. Le opzioni predefinite vengono utilizzate per il caricamento dei dati XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | Stream | Flusso di dati XML da utilizzare come origine dati. |
| xmlSchemaStream | Stream | Flusso di definizione dello schema XML che fornisce lo schema per i dati XML. |

### Guarda anche

* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Crea una nuova origine dati con dati da un file XML utilizzando le opzioni specificate per il caricamento dei dati XML.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | String | Percorso al file XML da utilizzare come origine dati. |
| options | XmlDataLoadOptions | Opzioni per il caricamento dei dati XML. |

### Guarda anche

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Crea una nuova origine dati con dati da un flusso XML utilizzando le opzioni specificate per il caricamento dei dati XML.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | Stream | Flusso di dati XML da utilizzare come origine dati. |
| options | XmlDataLoadOptions | Opzioni per il caricamento dei dati XML. |

### Guarda anche

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Crea una nuova origine dati con dati da un file XML utilizzando un file XML Schema Definition. Le opzioni specificate vengono utilizzate per il caricamento dei dati XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | String | Percorso al file XML da utilizzare come origine dati. |
| xmlSchemaPath | String | Percorso al file XML Schema Definition che fornisce lo schema per il file XML . |
| options | XmlDataLoadOptions | Opzioni per il caricamento dei dati XML. |

### Guarda anche

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Crea una nuova origine dati con dati provenienti da un flusso XML utilizzando un flusso XML Schema Definition. Le opzioni specificate vengono utilizzate per il caricamento dei dati XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | Stream | Flusso di dati XML da utilizzare come origine dati. |
| xmlSchemaStream | Stream | Flusso di definizione dello schema XML che fornisce lo schema per i dati XML. |
| options | XmlDataLoadOptions | Opzioni per il caricamento dei dati XML. |

### Guarda anche

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
