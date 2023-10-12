---
title: Class CsvDataSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Reporting.CsvDataSource clase. Proporciona acceso a los datos de un archivo CSV o secuencia para utilizarlos en un informe.
type: docs
weight: 4670
url: /es/net/aspose.words.reporting/csvdatasource/
---
## CsvDataSource class

Proporciona acceso a los datos de un archivo CSV o secuencia para utilizarlos en un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) artículo de documentación.

```csharp
public class CsvDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CsvDataSource](csvdatasource/#constructor)(Stream) | Crea una nueva fuente de datos con datos de una secuencia CSV usando opciones predeterminadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_2)(string) | Crea una nueva fuente de datos con datos de un archivo CSV usando opciones predeterminadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_1)(Stream, CsvDataLoadOptions) | Crea una nueva fuente de datos con datos de una secuencia CSV utilizando las opciones especificadas para analizar datos CSV. |
| [CsvDataSource](csvdatasource/#constructor_3)(string, CsvDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones especificadas para analizar datos CSV. |

### Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) .BuildReport sobrecargas.

En documentos de plantilla, un`CsvDataSource` La instancia debe tratarse de la misma manera que si fuera a.DataTable instancia. Para obtener más información, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Los tipos de datos de valores separados por comas se determinan automáticamente según sus representaciones de cadena. Entonces, en los documentos template , puede trabajar con valores escritos en lugar de solo cadenas. El motor es capaz de reconocer automáticamente valores de los siguientes tipos:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Tenga en cuenta que para que funcione el reconocimiento automático de tipos de datos, las representaciones de cadenas de valores separados por comas deben formarse utilizando configuraciones culturales invariantes.

Para anular el comportamiento predeterminado de la carga de datos CSV, inicialice y pase un[`CsvDataLoadOptions`](../csvdataloadoptions/) instancia a un constructor de esta clase.

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)


