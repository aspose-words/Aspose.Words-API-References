---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Reporting.JsonSimpleValueParseMode para un análisis JSON eficiente. ¡Maneje fácilmente valores nulos, booleanos, números y cadenas sin problemas!
type: docs
weight: 5440
url: /es/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Especifica un modo para analizar valores simples JSON (nulo, booleano, número, entero y cadena) mientras se carga JSON. Dicho modo no afecta el análisis de valores de fecha y hora.

```csharp
public enum JsonSimpleValueParseMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Loose | `0` | Especifica el modo en el que se determinan los tipos de valores simples JSON al analizar sus representaciones de cadena. Por ejemplo, el tipo de 'prop' del fragmento JSON '{ prop: "123" }' se determina como entero en este modo. |
| Strict | `1` | Especifica el modo en el que los tipos de valores simples JSON se determinan a partir de la propia notación JSON. Por ejemplo, el tipo de 'prop' del fragmento JSON '{ prop: "123" }' se determina como cadena en este modo. |

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
