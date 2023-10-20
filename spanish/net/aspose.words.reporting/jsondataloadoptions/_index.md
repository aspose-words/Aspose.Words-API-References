---
title: JsonDataLoadOptions Class
linktitle: JsonDataLoadOptions
articleTitle: JsonDataLoadOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Reporting.JsonDataLoadOptions clase. Representa opciones para analizar datos JSON en C#.
type: docs
weight: 4680
url: /es/net/aspose.words.reporting/jsondataloadoptions/
---
## JsonDataLoadOptions class

Representa opciones para analizar datos JSON.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) artículo de documentación.

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
| [AlwaysGenerateRootObject](../../aspose.words.reporting/jsondataloadoptions/alwaysgeneraterootobject/) { get; set; } | Obtiene o establece un indicador que indica si una fuente de datos generada siempre contendrá un objeto para un elemento JSON root . Si un elemento raíz JSON contiene una única propiedad compleja, dicho objeto no se crea de forma predeterminada. |
| [ExactDateTimeParseFormats](../../aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/) { get; set; } | Obtiene o establece formatos exactos para analizar valores de fecha y hora JSON mientras se carga JSON. El valor predeterminado es`nulo` . |
| [PreserveSpaces](../../aspose.words.reporting/jsondataloadoptions/preservespaces/) { get; set; } | Obtiene o establece una marca que indica si se deben conservar los espacios iniciales y finales al cargar valores string de datos JSON. |
| [SimpleValueParseMode](../../aspose.words.reporting/jsondataloadoptions/simplevalueparsemode/) { get; set; } | Obtiene o establece un modo para analizar valores JSON simples (nulo, booleano, número, entero y cadena) mientras se carga JSON. Este modo no afecta el análisis de los valores de fecha y hora. El valor predeterminado es Loose . |

## Observaciones

Una instancia de esta clase se puede pasar a los constructores de[`JsonDataSource`](../jsondatasource/) .

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
