---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „CsvDataLoadOptions Delimiter“, um Spaltentrennzeichen für effizientes Laden von Daten einfach anzupassen. Optimieren Sie Ihr Datenmanagement noch heute!
type: docs
weight: 30
url: /de/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Ruft das Zeichen ab, das als Spaltentrennzeichen verwendet werden soll, oder legt es fest.

```csharp
public char Delimiter { get; set; }
```

## Bemerkungen

Der Standardwert ist ',' (Komma).

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
