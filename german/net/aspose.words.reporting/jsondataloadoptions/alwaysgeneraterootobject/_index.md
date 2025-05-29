---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „JsonDataLoadOptions AlwaysGenerateRootObject“ Ihre JSON-Datenverarbeitung verbessert, indem sie ein konsistentes Stammobjekt für eine nahtlose Integration sicherstellt.
type: docs
weight: 20
url: /de/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Ruft ein Flag ab oder setzt es, das angibt, ob eine generierte Datenquelle immer ein Objekt für ein JSON-Stammelement enthält. Wenn ein JSON-Stammelement eine einzelne komplexe Eigenschaft enthält, wird ein solches Objekt standardmäßig nicht erstellt.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
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
