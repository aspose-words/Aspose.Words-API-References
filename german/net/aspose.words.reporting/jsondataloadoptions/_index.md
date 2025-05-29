---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Reporting.JsonDataLoadOptions für nahtloses JSON-Daten-Parsing. Verbessern Sie Ihre Dokumentenverarbeitung mit flexiblen Optionen!
type: docs
weight: 5420
url: /de/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Stellt Optionen zum Parsen von JSON-Daten dar.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class JsonDataLoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob eine generierte Datenquelle immer ein Objekt für ein JSON-Stammelement enthält. Wenn ein JSON-Stammelement eine einzelne komplexe Eigenschaft enthält, wird ein solches Objekt standardmäßig nicht erstellt. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Ruft genaue Formate für die Analyse von JSON-Datums- und Uhrzeitwerten beim Laden von JSON ab oder legt diese fest. Der Standardwert ist`null` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Ruft ein Flag ab oder legt ein Flag fest, das angibt, ob führende und nachfolgende Leerzeichen beim Laden von string Werten von JSON-Daten beibehalten werden sollen. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Ruft einen Modus für die Analyse einfacher JSON-Werte (Null, Boolean, Zahl, Integer und String) beim Laden von JSON ab oder legt ihn fest. Dieser Modus hat keinen Einfluss auf die Analyse von Datums- und Uhrzeitwerten. Der Standardwert ist Loose . |

## Bemerkungen

Eine Instanz dieser Klasse kann an Konstruktoren von übergeben werden[`JsonDataSource`](../jsondatasource/) .

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
