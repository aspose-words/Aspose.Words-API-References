---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die CommentChar-Eigenschaft in CsvDataLoadOptions anpassen, um die Verarbeitung Ihrer CSV-Daten zu verbessern. Optimieren Sie noch heute Ihr Datenladen!
type: docs
weight: 20
url: /de/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Ruft das Zeichen ab oder legt es fest, das zum Kommentieren von Zeilen in CSV-Daten verwendet wird.

```csharp
public char CommentChar { get; set; }
```

## Bemerkungen

Der Standardwert ist „#“ (Nummernzeichen).

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
