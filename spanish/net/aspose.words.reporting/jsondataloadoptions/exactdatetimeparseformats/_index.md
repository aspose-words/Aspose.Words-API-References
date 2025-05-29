---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words para .NET
description: Descubra ExactDateTimeParseFormats de JsonDataLoadOptions para un análisis preciso de fecha y hora JSON. ¡Personalice los formatos fácilmente para una carga de datos fluida!
type: docs
weight: 30
url: /es/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Obtiene o establece los formatos exactos para analizar valores de fecha y hora JSON al cargar JSON. El valor predeterminado es`nulo` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Observaciones

Las cadenas codificadas con el formato de fecha y hora JSON de Microsoft® (por ejemplo, "/Date(1224043200000)/") siempre se reconocen como valores de fecha y hora, independientemente del valor de esta propiedad. La propiedad define formatos adicionales que se utilizan al analizar valores de fecha y hora de cadenas de la siguiente manera:

* Cuando`ExactDateTimeParseFormats` es`nulo` , el formato ISO-8601 y todos los formatos de fecha y hora admitidos para las culturas actuales, inglés de EE. UU. e inglés de Nueva Zelanda se utilizan adicionalmente en el orden mencionado.
* Cuando`ExactDateTimeParseFormats`contiene cadenas, se utilizan como formatos de fecha y hora adicionales que utilizan la cultura actual.
* Cuando`ExactDateTimeParseFormats` está vacío, no se utilizan formatos de fecha y hora adicionales.

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
