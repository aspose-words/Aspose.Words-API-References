---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words per .NET
description: Genera senza sforzo report pronti all'uso con il metodo BuildReport di ReportingEngine, popolando senza problemi i modelli con i dati provenienti dalla fonte scelta.
type: docs
weight: 50
url: /it/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Popola il documento modello specificato con dati provenienti dalla fonte specificata, rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto sorgente dati. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto successo. Il flag restituito ha senso solo se un valore di[`Options`](../options/) la proprietà include ilInlineErrorMessages opzione.

## Osservazioni

Utilizzando questo overload è possibile fare riferimento ai membri dell'origine dati nel documento modello, ma non è possibile fare riferimento all'oggetto origine dati stesso. È necessario utilizzare`BuildReport` sovraccarico per raggiungere questo obiettivo.

Un oggetto sorgente dati può essere di uno dei seguenti tipi:

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
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipi diversi nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Popola il documento modello specificato con dati provenienti dalla fonte specificata, rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSource | Object | Un oggetto sorgente dati. |
| dataSourceName | String | Un nome per fare riferimento all'oggetto origine dati nel modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto successo. Il flag restituito ha senso solo se un valore di[`Options`](../options/) la proprietà include ilInlineErrorMessages opzione.

## Osservazioni

Utilizzando questo sovraccarico è possibile fare riferimento ai membri dell'origine dati e all'oggetto origine dati stesso nel modello. Se non si intende fare riferimento all'oggetto origine dati stesso, è possibile omettere*dataSourceName* passaggio`null` oppure utilizzare il`BuildReport` sovraccarico.

Un oggetto sorgente dati può essere di uno dei seguenti tipi:

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
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipi diversi nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Esempi

Mostra come consentire l'accesso ai membri mancanti.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Mostra come rimuovere paragrafi in modo selettivo.

```csharp
// Il modello contiene tag con un punto esclamativo. Per tali tag, i paragrafi vuoti verranno rimossi.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Mostra come visualizzare i valori come testo in dollari.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Popola il documento modello specificato con dati provenienti dalle fonti specificate, rendendolo un report pronto.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | Document | Un documento modello da compilare con i dati. |
| dataSources | Object[] | Un array di oggetti di origine dati. |
| dataSourceNames | String[] | Una matrice di nomi per fare riferimento agli oggetti sorgente dati all'interno del modello. |

### Valore di ritorno

Un flag che indica se l'analisi del documento modello ha avuto successo. Il flag restituito ha senso solo se un valore di[`Options`](../options/) la proprietà include ilInlineErrorMessages opzione.

## Osservazioni

Utilizzando questo sovraccarico è possibile fare riferimento a più oggetti di origine dati e ai loro membri nel modello. Il nome della prima origine dati può essere omesso (ad esempio, essere una stringa vuota o`null` se si intende fare riferimento con ai membri dell'origine dati ma non all'oggetto origine dati stesso. I nomi delle altre origini dati devono essere specificati e univoci.

Se si intende utilizzare una singola fonte di dati, prendere in considerazione l'utilizzo di`BuildReport` e`BuildReport` sovraccarichi invece.

Un oggetto sorgente dati può essere di uno dei seguenti tipi:

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
* Qualsiasi altro tipo .NET arbitrario non dinamico e non anonimo

Per informazioni su come lavorare con origini dati di tipi diversi nei documenti modello, vedere il riferimento alla sintassi del modello (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Esempi

Mostra come lavorare con i grafici di Word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Mostra come mantenere invariata la numerazione inserita.

```csharp
// Per impostazione predefinita, gli elenchi numerati di un documento modello vengono continuati quando i loro identificatori corrispondono a quelli di un documento che viene inserito.
// Con "-sourceNumbering" la numerazione dovrebbe essere separata e mantenuta così com'è.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
