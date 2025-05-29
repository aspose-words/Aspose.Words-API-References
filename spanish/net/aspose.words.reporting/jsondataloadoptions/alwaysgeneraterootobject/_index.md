---
title: JsonDataLoadOptions.AlwaysGenerateRootObject
linktitle: AlwaysGenerateRootObject
articleTitle: AlwaysGenerateRootObject
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad AlwaysGenerateRootObject de JsonDataLoadOptions mejora el manejo de datos JSON al garantizar un objeto raíz consistente para una integración perfecta.
type: docs
weight: 20
url: /es/net/aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/
---
## JsonDataLoadOptions.AlwaysGenerateRootObject property

Obtiene o establece un indicador que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz JSON . Si un elemento raíz JSON contiene una sola propiedad compleja, dicho objeto no se crea por defecto.

```csharp
public bool AlwaysGenerateRootObject { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

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
