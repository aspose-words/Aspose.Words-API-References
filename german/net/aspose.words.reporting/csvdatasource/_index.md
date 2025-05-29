---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf CSV-Daten zu und nutzen Sie sie mit Aspose.Words.Reporting.CsvDataSource. Optimieren Sie Ihre Berichte durch nahtlose Datenintegration!
type: docs
weight: 5410
url: /de/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Bietet Zugriff auf Daten einer CSV-Datei oder eines Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class CsvDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung der Standardoptionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der Standardoptionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten. |

## Bemerkungen

Um beim Generieren eines Berichts auf die Daten der entsprechenden Datei oder des Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an einen der[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

In Vorlagendokumenten kann ein`CsvDataSource` Instanz sollte auf die gleiche Weise behandelt werden, als wäre sie eineDataTable -Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Die Datentypen kommagetrennter Werte werden automatisch anhand ihrer Zeichenfolgendarstellung bestimmt. Daher können Sie in Vorlagendokumenten mit typisierten Werten statt nur mit Zeichenfolgen arbeiten. Die Engine erkennt -Werte der folgenden Typen automatisch:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Beachten Sie, dass für die automatische Erkennung von Datentypen Zeichenfolgendarstellungen von durch Kommas getrennten Werten unter Verwendung invarianter Kultureinstellungen erstellt werden sollten.

Um das Standardverhalten des CSV-Datenladens zu überschreiben, initialisieren und übergeben Sie ein[`CsvDataLoadOptions`](../csvdataloadoptions/) instance zu einem Konstruktor dieser Klasse.

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
