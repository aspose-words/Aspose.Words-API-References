---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words für .NET
description: Aspose.Words.Reporting.CsvDataSource klas. Bietet Zugriff auf Daten einer CSVDatei oder eines CSVStreams zur Verwendung in einem Bericht in C#.
type: docs
weight: 4670
url: /de/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Bietet Zugriff auf Daten einer CSV-Datei oder eines CSV-Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Reporting-Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class CsvDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung von Standardoptionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der Standardoptionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem CSV-Stream unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer CSV-Datei unter Verwendung der angegebenen Optionen zum Parsen von CSV-Daten. |

## Bemerkungen

Um beim Erstellen eines Berichts auf Daten der entsprechenden Datei oder des entsprechenden Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an eine von[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

In Vorlagendokumenten a`CsvDataSource` Die Instanz sollte genauso behandelt werden, als ob sie a wäreDataTable Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Datentypen von durch Kommas getrennten Werten werden automatisch anhand ihrer Zeichenfolgendarstellungen bestimmt. In template -Dokumenten können Sie also mit typisierten Werten statt nur mit Zeichenfolgen arbeiten. Die Engine ist in der Lage, -Werte der folgenden Typen automatisch zu erkennen:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Beachten Sie, dass Zeichenfolgendarstellungen durch Kommas getrennter Werte unter Verwendung invarianter Kultureinstellungen erstellt werden sollten, damit die automatische Erkennung von Datentypen funktioniert.

Um das Standardverhalten beim Laden von CSV-Daten zu überschreiben, initialisieren und übergeben Sie a[`CsvDataLoadOptions`](../csvdataloadoptions/) Instanz an einen Konstruktor dieser Klasse.

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
