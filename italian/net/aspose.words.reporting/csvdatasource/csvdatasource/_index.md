---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words per .NET
description: Crea facilmente una potente sorgente dati CSV con il nostro costruttore CsvDataSource. Semplifica l'analisi dei dati con opzioni predefinite per un'integrazione perfetta.
type: docs
weight: 10
url: /it/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Crea una nuova origine dati con dati da un file CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV.

```csharp
public CsvDataSource(string csvPath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvPath | String | Percorso al file CSV da utilizzare come origine dati. |

### Guarda anche

* class [CsvDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Crea una nuova origine dati con dati da un file CSV utilizzando le opzioni specificate per l'analisi dei dati CSV.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvPath | String | Percorso al file CSV da utilizzare come origine dati. |
| options | CsvDataLoadOptions | Opzioni per l'analisi dei dati CSV. |

## Esempi

Mostra come utilizzare CSV come origine dati (stringa).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Guarda anche

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Crea una nuova origine dati con dati da un flusso CSV utilizzando le opzioni predefinite per l'analisi dei dati CSV.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvStream | Stream | Flusso di dati CSV da utilizzare come origine dati. |

### Guarda anche

* class [CsvDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Crea una nuova origine dati con dati da un flusso CSV utilizzando le opzioni specificate per l'analisi dei dati CSV.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| csvStream | Stream | Flusso di dati CSV da utilizzare come origine dati. |
| options | CsvDataLoadOptions | Opzioni per l'analisi dei dati CSV. |

## Esempi

Mostra come utilizzare CSV come origine dati (flusso).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Guarda anche

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* spazio dei nomi [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assemblea [Aspose.Words](../../../)
