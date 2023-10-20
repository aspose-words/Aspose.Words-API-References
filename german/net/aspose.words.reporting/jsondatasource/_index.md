---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words für .NET
description: Aspose.Words.Reporting.JsonDataSource klas. Bietet Zugriff auf Daten einer JSONDatei oder eines JSONStreams zur Verwendung in einem Bericht in C#.
type: docs
weight: 4690
url: /de/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Bietet Zugriff auf Daten einer JSON-Datei oder eines JSON-Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Reporting-Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class JsonDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung von Standardoptionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung von Standardoptionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten. |

## Bemerkungen

Um beim Erstellen eines Berichts auf Daten der entsprechenden Datei oder des entsprechenden Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an eine von[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

Wenn in Vorlagendokumenten ein JSON-Element der obersten Ebene ein Array ist, a`JsonDataSource` Die Instanz sollte genauso behandelt werden, als wäre sie eineDataTable Instanz. Wenn ein JSON-Element der obersten Ebene ein Objekt ist, a`JsonDataSource` Die Instanz sollte genauso behandelt werden, als wäre sie aDataRow Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

In Vorlagendokumenten können Sie mit typisierten Werten von JSON-Elementen arbeiten. Der Einfachheit halber ersetzt die Engine den Satz der einfachen JSON-Typen durch den folgenden:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Die Engine erkennt automatisch Werte der zusätzlichen Typen anhand ihrer JSON-Darstellungen.

Um das Standardverhalten beim Laden von JSON-Daten zu überschreiben, initialisieren und übergeben Sie a[`JsonDataLoadOptions`](../jsondataloadoptions/) Instanz an einen Konstruktor dieser Klasse.

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
