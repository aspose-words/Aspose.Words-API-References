---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Reporting.CsvDataLoadOptions für effizientes CSV-Datenparsing. Optimieren Sie Ihre Dokumentenverarbeitung noch heute mit anpassbaren Optionen!
type: docs
weight: 5400
url: /de/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Stellt Optionen zum Parsen von CSV-Daten dar.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class CsvDataLoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Initialisiert eine neue Instanz dieser Klasse und gibt in der ersten Zeile an, ob CSV-Daten Spaltennamen enthalten. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Ruft das Zeichen ab oder legt es fest, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Ruft das Zeichen ab, das als Spaltentrennzeichen verwendet werden soll, oder legt es fest. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der erste Datensatz der CSV-Daten Spaltennamen enthält. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Ruft das Zeichen ab oder legt es fest, das zum Anführen von Feldwerten verwendet wird. |

## Bemerkungen

Eine Instanz dieser Klasse kann an Konstruktoren von übergeben werden[`CsvDataSource`](../csvdatasource/) .

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

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
