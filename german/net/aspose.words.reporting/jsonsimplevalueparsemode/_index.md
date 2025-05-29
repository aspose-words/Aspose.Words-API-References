---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Reporting.JsonSimpleValueParseMode für effizientes JSON-Parsing. Verarbeiten Sie Nullen, Boolesche Werte, Zahlen und Zeichenfolgen problemlos!
type: docs
weight: 5440
url: /de/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Gibt einen Modus zum Parsen einfacher JSON-Werte (Null, Boolean, Zahl, Integer und String) beim Laden von JSON an. Dieser Modus hat keinen Einfluss auf das Parsen von Datums-/Uhrzeitwerten.

```csharp
public enum JsonSimpleValueParseMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Loose | `0` | Gibt den Modus an, in dem Typen einfacher JSON-Werte beim Parsen ihrer Zeichenfolgendarstellungen bestimmt werden. Beispielsweise wird der Typ von „prop“ aus dem JSON-Snippet „{ prop: "123" }“ in diesem Modus als Ganzzahl bestimmt. |
| Strict | `1` | Gibt den Modus an, in dem die Typen einfacher JSON-Werte aus der JSON-Notation selbst bestimmt werden. Beispielsweise wird der Typ von „prop“ aus dem JSON-Snippet „{ prop: "123" }“ in diesem Modus als Zeichenfolge bestimmt. |

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
