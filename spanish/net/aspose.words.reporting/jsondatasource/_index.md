---
title: JsonDataSource Class
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: Aspose.Words para .NET
description: Desbloquee informes potentes con Aspose.Words.Reporting.JsonDataSource. Acceda fácilmente a datos JSON para una integración perfecta en sus informes.
type: docs
weight: 5430
url: /es/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Proporciona acceso a los datos de un archivo o flujo JSON para ser utilizados dentro de un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

```csharp
public class JsonDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(*Stream*) | Crea una nueva fuente de datos con datos de una secuencia JSON utilizando las opciones predeterminadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(*string*) | Crea una nueva fuente de datos con datos de un archivo JSON utilizando las opciones predeterminadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(*Stream, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nueva fuente de datos con datos de una secuencia JSON utilizando las opciones especificadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(*string, [JsonDataLoadOptions](../jsondataloadoptions/)*) | Crea una nueva fuente de datos con datos de un archivo JSON utilizando las opciones especificadas para analizar datos JSON. |

## Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras se genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) Sobrecargas de .BuildReport.

En los documentos de plantilla, si un elemento JSON de nivel superior es una matriz,`JsonDataSource` La instancia debe ser tratada de la misma manera que si fuera unaDataTableInstancia . Si un elemento JSON de nivel superior es un objeto,`JsonDataSource` La instancia debe tratarse de la misma manera que si fuera unaDataRow Instancia . Para más información, consulte la referencia de sintaxis de plantillas (https://docs.aspose.com/display/wordsnet/Template+Syntax).

En los documentos de plantilla, se puede trabajar con valores tipificados de elementos JSON. Para mayor comodidad, el motor reemplaza el conjunto de tipos simples JSON por el siguiente:

* Nullable
* Nullable
* Nullable
* Nullable
* String

El motor reconoce automáticamente los valores de los tipos adicionales en sus representaciones JSON.

Para anular el comportamiento predeterminado de la carga de datos JSON, inicialice y pase un[`JsonDataLoadOptions`](../jsondataloadoptions/) instance a un constructor de esta clase.

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
