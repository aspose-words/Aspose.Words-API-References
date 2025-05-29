---
title: JsonDataLoadOptions
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor JsonDataLoadOptions, inicialice sin esfuerzo la carga de datos con configuraciones predeterminadas personalizables para un rendimiento óptimo.
type: docs
weight: 10
url: /es/net/aspose.words.reporting/jsondataloadoptions/jsondataloadoptions/
---
## JsonDataLoadOptions constructor

Inicializa una nueva instancia de esta clase con opciones predeterminadas.

```csharp
public JsonDataLoadOptions()
```

## Ejemplos

Muestra cómo utilizar JSON como fuente de datos (cadena).

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

### Ver también

* class [JsonDataLoadOptions](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
