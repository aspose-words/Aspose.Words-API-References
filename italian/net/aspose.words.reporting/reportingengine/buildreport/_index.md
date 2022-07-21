---
title: BuildReport
second_title: Aspose.Words per .NET API Reference
description: Popola il documento modello specificato con i dati dellorigine specificata rendendolo un report pronto.
type: docs
weight: 40
url: /it/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Popola il documento modello specificato con i dati dell'origine specificata rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto origine dati. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello è riuscita. Il flag restituito ha senso solo se un valore del[`Options`](../options)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo overload è possibile fare riferimento ai membri dell'origine dati nel documento modello, ma non è possibile fare riferimento all'oggetto origine dati stesso. Dovresti usare il[`BuildReport`](../buildreport) sovraccarico per raggiungere questo obiettivo.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipo diverso nei documenti modello, vedere riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Popola il documento modello specificato con i dati dell'origine specificata rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto origine dati. |
| dataSourceName | String | Un nome per fare riferimento all'oggetto origine dati nel modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello è riuscita. Il flag restituito ha senso solo se un valore del[`Options`](../options)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo overload è possibile fare riferimento ai membri dell'origine dati e all'oggetto origine dati stesso nel modello. Se non hai intenzione di fare riferimento all'oggetto origine dati stesso, puoi ometterlo*dataSourceName* passando null o usa il[`BuildReport`](../buildreport) sovraccarico.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipo diverso nei documenti modello, vedere riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Popola il documento modello specificato con i dati delle origini specificate rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSources | Object[] | Una matrice di oggetti origine dati. |
| dataSourceNames | String[] | Una matrice di nomi per fare riferimento agli oggetti origine dati all'interno del modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello è riuscita. Il flag restituito ha senso solo se un valore del[`Options`](../options)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo overload è possibile fare riferimento a più oggetti origine dati e ai relativi membri nel modello. Il nome della prima origine dati può essere omesso (ovvero essere una stringa vuota o null) se si intende fare riferimento ai membri dell'origine dati ma non all'oggetto origine dati stesso. I nomi delle altre origini dati devono essere specificati e univoci.

Se intendi utilizzare una singola origine dati, considera l'utilizzo di[`BuildReport`](../buildreport) e[`BuildReport`](../buildreport) sovraccarichi invece.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource)
* [`JsonDataSource`](../../jsondatasource)
* [`CsvDataSource`](../../csvdatasource)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipo diverso nei documenti modello, vedere riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document)
* class [ReportingEngine](../../reportingengine)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
