---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words per .NET
description: Sblocca potenti funzionalità di reporting con Aspose.Words.XmlDataSource. Accedi facilmente ai dati XML per integrarli perfettamente nei tuoi report e migliorare la visualizzazione dei dati.
type: docs
weight: 5490
url: /it/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Fornisce l'accesso ai dati di un file XML o di un flusso da utilizzare all'interno di un report.

Per saperne di più, visita il[Motore di reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) articolo di documentazione.

```csharp
public class XmlDataSource
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Crea una nuova origine dati con dati da un flusso XML utilizzando le opzioni predefinite per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Crea una nuova origine dati con dati da un file XML utilizzando le opzioni predefinite per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Crea una nuova origine dati con dati provenienti da un flusso XML utilizzando un flusso XML Schema Definition. Le opzioni predefinite vengono utilizzate per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nuova origine dati con dati da un flusso XML utilizzando le opzioni specificate per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Crea una nuova origine dati con dati da un file XML utilizzando un file XML Schema Definition. Le opzioni predefinite vengono utilizzate per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nuova origine dati con dati da un file XML utilizzando le opzioni specificate per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nuova origine dati con dati provenienti da un flusso XML utilizzando un flusso XML Schema Definition. Le opzioni specificate vengono utilizzate per il caricamento dei dati XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crea una nuova origine dati con dati da un file XML utilizzando un file XML Schema Definition. Le opzioni specificate vengono utilizzate per il caricamento dei dati XML. |

## Osservazioni

Per accedere ai dati del file o del flusso corrispondente durante la generazione di un report, passare un'istanza di questa classe come una fonte dati a uno dei[`ReportingEngine`](../reportingengine/) Sovraccarichi di .BuildReport.

Nei documenti modello, se un elemento XML di primo livello contiene solo un elenco di elementi dello stesso tipo, un`XmlDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse aDataTable istanza. Altrimenti, un`XmlDataSource` l'istanza dovrebbe essere trattata allo stesso modo come se fosse aDataRow Istanza . Per ulteriori informazioni, consultare il riferimento alla sintassi del template (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Quando la definizione dello schema XML viene passata a un costruttore di questa classe, i tipi di dati dei valori degli elementi XML semplici e degli attributi vengono determinati in base allo schema. Pertanto, nei documenti modello, è possibile lavorare con valori tipizzati anziché solo stringhe.

Quando la definizione dello schema XML non viene passata a un costruttore di questa classe, i tipi di dati dei valori degli elementi XML semplici e degli attributi vengono determinati automaticamente in base alle loro rappresentazioni di stringa. Pertanto, nei documenti modello, è possibile lavorare con anche in questo caso con valori tipizzati. Il motore è in grado di riconoscere automaticamente i seguenti tipi di valori:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Si noti che affinché il riconoscimento automatico dei tipi di dati funzioni, le rappresentazioni stringa dei valori degli elementi XML semplici e degli attributi devono essere formate utilizzando impostazioni di cultura invarianti.

Per sovrascrivere il comportamento predefinito del caricamento dei dati XML, inizializzare e passare un[`XmlDataLoadOptions`](../xmldataloadoptions/) istanza a un costruttore di questa classe.

## Esempi

Mostra come utilizzare XML come origine dati (stringa).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

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

* spazio dei nomi [Aspose.Words.Reporting](../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../)
