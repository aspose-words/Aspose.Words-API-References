---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: Aspose.Words für .NET
description: Entdecken Sie die QuoteChar-Eigenschaft von CsvDataLoadOptions, um die Anführungszeichen für Feldwerte einfach anzupassen und so eine nahtlose Datenverarbeitung und verbesserte CSV-Verwaltung zu ermöglichen.
type: docs
weight: 50
url: /de/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Ruft das Zeichen ab oder legt es fest, das zum Anführen von Feldwerten verwendet wird.

```csharp
public char QuoteChar { get; set; }
```

## Bemerkungen

Der Standardwert ist „“ (Anführungszeichen).

Verdoppeln Sie das Zeichen, um es in zitierten Text einzufügen.

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
