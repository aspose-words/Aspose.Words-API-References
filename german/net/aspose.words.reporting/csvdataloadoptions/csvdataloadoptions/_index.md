---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den CsvDataLoadOptions-Konstruktor – initialisieren Sie ihn einfach mit Standardeinstellungen für effizientes Laden von Daten und nahtlose Integration.
type: docs
weight: 10
url: /de/net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen.

```csharp
public CsvDataLoadOptions()
```

## Beispiele

Zeigt, wie CSV als Datenquelle (Zeichenfolge) verwendet wird.

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

### Siehe auch

* class [CsvDataLoadOptions](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse und gibt in der ersten Zeile an, ob CSV-Daten Spaltennamen enthalten.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

## Beispiele

Zeigt, wie CSV als Datenquelle (Zeichenfolge) verwendet wird.

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

### Siehe auch

* class [CsvDataLoadOptions](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
