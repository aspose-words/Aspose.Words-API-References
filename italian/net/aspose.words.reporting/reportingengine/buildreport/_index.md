---
title: ReportingEngine.BuildReport
second_title: Aspose.Words per .NET API Reference
description: ReportingEngine metodo. Compila il documento modello specificato con i dati provenienti dallorigine specificata rendendolo un report pronto.
type: docs
weight: 40
url: /it/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Compila il documento modello specificato con i dati provenienti dall'origine specificata rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto origine dati. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto esito positivo. Il flag restituito ha senso solo se un valore del[`Options`](../options/)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo sovraccarico è possibile fare riferimento ai membri dell'origine dati nel documento modello, ma non è possibile fare riferimento all'oggetto origine dati stesso. Dovresti usare il`BuildReport` sovraccarico per raggiungere questo obiettivo.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario, non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di diverso tipo nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine/)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Compila il documento modello specificato con i dati provenienti dall'origine specificata rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto origine dati. |
| dataSourceName | String | Un nome per fare riferimento all'oggetto origine dati nel modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto esito positivo. Il flag restituito ha senso solo se un valore del[`Options`](../options/)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo sovraccarico è possibile fare riferimento ai membri dell'origine dati e all'oggetto origine dati stesso nel modello. Se non intendi fare riferimento all'oggetto origine dati stesso, puoi ometterlo*dataSourceName* passaggio`nullo` oppure usa il`BuildReport` sovraccarico.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario, non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di diverso tipo nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine/)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Compila il documento modello specificato con i dati provenienti dalle origini specificate rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSources | Object[] | Un array di oggetti origine dati. |
| dataSourceNames | String[] | Un array di nomi per fare riferimento agli oggetti origine dati all'interno del modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto esito positivo. Il flag restituito ha senso solo se un valore del[`Options`](../options/)la proprietà include ilInlineErrorMessages opzione.

### Osservazioni

Utilizzando questo sovraccarico è possibile fare riferimento a più oggetti origine dati e ai relativi membri nel modello. Il nome della prima origine dati può essere omesso (cioè essere una stringa vuota oppure`nullo` se intendi fare riferimento ai membri dell'origine dati ma non all'oggetto origine dati stesso. I nomi delle altre origini dati devono essere specificati e univoci.

Se intendi utilizzare un'unica origine dati, considera l'utilizzo di of`BuildReport` e`BuildReport` invece si sovraccarica.

Un oggetto origine dati può essere di uno dei seguenti tipi:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Qualsiasi altro tipo .NET arbitrario, non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di diverso tipo nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../reportingengine/)
* assemblea [Aspose.Words](../../../)


