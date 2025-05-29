---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words für .NET
description: Entdecken Sie die ExactDateTimeParseFormats von JsonDataLoadOptions für präzises JSON-Datums-/Uhrzeit-Parsing. Passen Sie Formate einfach an, um Daten nahtlos zu laden!
type: docs
weight: 30
url: /de/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Ruft genaue Formate für die Analyse von JSON-Datums- und Uhrzeitwerten beim Laden von JSON ab oder legt diese fest. Der Standardwert ist`null` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Bemerkungen

Zeichenfolgen, die im Microsoft® JSON-Datums-/Uhrzeitformat kodiert sind (z. B. "/Date(1224043200000)/"), werden unabhängig vom Wert dieser Eigenschaft immer als Datums-/Uhrzeitwerte erkannt. Die Eigenschaft definiert zusätzliche Formate, die beim Parsen von Datums-/Uhrzeitwerten aus Zeichenfolgen wie folgt verwendet werden:

* Wann`ExactDateTimeParseFormats` Ist`null` , das ISO-8601-Format und alle für die aktuelle Kultur, die US-amerikanische Sprache und die neuseeländische Sprache unterstützten Datums-/Uhrzeitformate werden zusätzlich in der genannten Reihenfolge verwendet.
* Wann`ExactDateTimeParseFormats`Enthält Zeichenfolgen. Diese werden als zusätzliche Datums-/Uhrzeitformate unter Verwendung der aktuellen Kultur verwendet.
* Wann`ExactDateTimeParseFormats` ist leer, es werden keine zusätzlichen Datums-/Uhrzeitformate verwendet.

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

* class [JsonDataLoadOptions](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
