---
title: JsonDataLoadOptions.PreserveSpaces
linktitle: PreserveSpaces
articleTitle: PreserveSpaces
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „JsonDataLoadOptions PreserveSpaces“ die Verarbeitung von JSON-Daten verbessert, indem führende und nachfolgende Leerzeichen für genaue Zeichenfolgenwerte beibehalten werden.
type: docs
weight: 40
url: /de/net/aspose.words.reporting/jsondataloadoptions/preservespaces/
---
## JsonDataLoadOptions.PreserveSpaces property

Ruft ein Flag ab oder legt ein Flag fest, das angibt, ob führende und nachfolgende Leerzeichen beim Laden von string Werten von JSON-Daten beibehalten werden sollen.

```csharp
public bool PreserveSpaces { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

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
