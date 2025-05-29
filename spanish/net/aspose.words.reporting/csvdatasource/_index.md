---
title: CsvDataSource Class
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words para .NET
description: Acceda y utilice datos CSV fácilmente con Aspose.Words.Reporting.CsvDataSource. ¡Mejore sus informes con una integración de datos fluida!
type: docs
weight: 5410
url: /es/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Proporciona acceso a los datos de un archivo CSV o una secuencia para utilizarlos en un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

```csharp
public class CsvDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(*Stream*) | Crea una nueva fuente de datos con datos de una secuencia CSV utilizando las opciones predeterminadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(*string*) | Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones predeterminadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(*Stream, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nueva fuente de datos con datos de una secuencia CSV utilizando las opciones especificadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(*string, [CsvDataLoadOptions](../csvdataloadoptions/)*) | Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones especificadas para analizar datos CSV. |

## Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras se genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) Sobrecargas de .BuildReport.

En los documentos de plantilla, un`CsvDataSource` La instancia debe tratarse de la misma manera que si fuera unaDataTableInstancia . Para más información, consulte la referencia de sintaxis de plantillas (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Los tipos de datos de los valores separados por comas se determinan automáticamente a partir de sus representaciones en cadenas. Por lo tanto, en los documentos template , puede trabajar con valores tipificados en lugar de solo cadenas. El motor puede reconocer automáticamente valores de los siguientes tipos:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Tenga en cuenta que para que funcione el reconocimiento automático de tipos de datos, las representaciones de cadena de valores separados por comas deben formarse utilizando configuraciones culturales invariantes.

Para anular el comportamiento predeterminado de la carga de datos CSV, inicialice y pase un[`CsvDataLoadOptions`](../csvdataloadoptions/) instance a un constructor de esta clase.

## Ejemplos

Muestra cómo utilizar CSV como fuente de datos (cadena).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
