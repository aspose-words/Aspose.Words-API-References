---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words für .NET
description: Schalten Sie leistungsstarke Berichte mit Aspose.Words.Reporting.JsonDataSource frei. Greifen Sie einfach auf JSON-Daten zu und integrieren Sie diese nahtlos in Ihre Berichte.
type: docs
weight: 5430
url: /de/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Bietet Zugriff auf Daten einer JSON-Datei oder eines JSON-Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class JsonDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung der Standardoptionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung der Standardoptionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem JSON-Stream unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer JSON-Datei unter Verwendung der angegebenen Optionen zum Parsen von JSON-Daten. |

## Bemerkungen

Um beim Generieren eines Berichts auf die Daten der entsprechenden Datei oder des Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an einen der[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

Wenn in Vorlagendokumenten ein JSON-Element der obersten Ebene ein Array ist,`JsonDataSource` Instanz sollte auf die gleiche Weise behandelt werden, als wäre sie eineDataTable Instanz. Wenn ein JSON-Element der obersten Ebene ein Objekt ist,`JsonDataSource` Instanz sollte genauso behandelt werden, als wäre sie aDataRow -Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

In Vorlagendokumenten können Sie mit typisierten Werten von JSON-Elementen arbeiten. Der Einfachheit halber ersetzt die Engine den Satz einfacher JSON-Typen durch den folgenden:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Die Engine erkennt die Werte der zusätzlichen Typen automatisch anhand ihrer JSON-Darstellungen.

Um das Standardverhalten des JSON-Datenladens zu überschreiben, initialisieren und übergeben Sie ein[`JsonDataLoadOptions`](../jsondataloadoptions/) instance zu einem Konstruktor dieser Klasse.

## Beispiele

Zeigt, wie JSON als Datenquelle (Zeichenfolge) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
