---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: Aspose.Words für .NET
description: Entdecken Sie die HasHeaders-Eigenschaft von CsvDataLoadOptions, um CSV-Importe einfach zu verwalten, indem Sie angeben, ob der erste Datensatz Spaltennamen für eine nahtlose Datenintegration enthält.
type: docs
weight: 40
url: /de/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält.

```csharp
public bool HasHeaders { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

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
