---
title: JsonDataLoadOptions.SimpleValueParseMode
linktitle: SimpleValueParseMode
articleTitle: SimpleValueParseMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SimpleValueParseMode-Eigenschaft in JsonDataLoadOptions die JSON-Analyse für Nullwerte, Boolesche Werte, Zahlen und Zeichenfolgen verbessert. Optimieren Sie noch heute Ihr Datenladen!
type: docs
weight: 50
url: /de/net/aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/
---
## JsonDataLoadOptions.SimpleValueParseMode property

Ruft einen Modus für die Analyse einfacher JSON-Werte (Null, Boolean, Zahl, Integer und String) beim Laden von JSON ab oder legt ihn fest. Dieser Modus hat keinen Einfluss auf die Analyse von Datums- und Uhrzeitwerten. Der Standardwert ist Loose .

```csharp
public JsonSimpleValueParseMode SimpleValueParseMode { get; set; }
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

* enum [JsonSimpleValueParseMode](../../jsonsimplevalueparsemode/)
* class [JsonDataLoadOptions](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
