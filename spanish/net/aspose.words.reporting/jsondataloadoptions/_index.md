---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Reporting.JsonDataLoadOptions para un análisis fluido de datos JSON. ¡Mejore el procesamiento de sus documentos con opciones flexibles!
type: docs
weight: 5420
url: /es/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Representa opciones para analizar datos JSON.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

```csharp
public class JsonDataLoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [JsonDataLoadOptions](jsondataloadoptions/)() | Inicializa una nueva instancia de esta clase con opciones predeterminadas. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Obtiene o establece un indicador que indica si una fuente de datos generada siempre contendrá un objeto para un elemento raíz JSON . Si un elemento raíz JSON contiene una sola propiedad compleja, dicho objeto no se crea por defecto. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Obtiene o establece los formatos exactos para analizar valores de fecha y hora JSON al cargar JSON. El valor predeterminado es`nulo` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Obtiene o establece un indicador que indica si se deben conservar los espacios iniciales y finales al cargar valores de cadena de datos JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Obtiene o establece un modo para analizar valores simples JSON (null, boolean, number, entire y string) al cargar JSON. Este modo no afecta el análisis de valores de fecha y hora. El valor predeterminado es Loose . |

## Observaciones

Se puede pasar una instancia de esta clase a los constructores de[`JsonDataSource`](../jsondatasource/) .

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

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
