---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den JsonDataLoadOptions-Konstruktor und initialisieren Sie mühelos das Laden Ihrer Daten mit anpassbaren Standardeinstellungen für optimale Leistung.
type: docs
weight: 10
url: /de/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen.

```csharp
public JsonDataLoadOptions()
```

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
