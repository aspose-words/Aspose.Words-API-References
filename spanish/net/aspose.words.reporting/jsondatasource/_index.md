---
title: Class JsonDataSource
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Reporting.JsonDataSource clase. Proporciona acceso a los datos de un archivo o secuencia JSON que se utilizarán en un informe.
type: docs
weight: 4690
url: /es/net/aspose.words.reporting/jsondatasource/
---
## JsonDataSource class

Proporciona acceso a los datos de un archivo o secuencia JSON que se utilizarán en un informe.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) artículo de documentación.

```csharp
public class JsonDataSource
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [JsonDataSource](jsondatasource/#constructor)(Stream) | Crea una nueva fuente de datos con datos de una secuencia JSON usando opciones predeterminadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_2)(string) | Crea una nueva fuente de datos con datos de un archivo JSON usando opciones predeterminadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_1)(Stream, JsonDataLoadOptions) | Crea una nueva fuente de datos con datos de una secuencia JSON utilizando las opciones especificadas para analizar datos JSON. |
| [JsonDataSource](jsondatasource/#constructor_3)(string, JsonDataLoadOptions) | Crea una nueva fuente de datos con datos de un archivo JSON usando las opciones especificadas para analizar datos JSON. |

### Observaciones

Para acceder a los datos del archivo o flujo correspondiente mientras genera un informe, pase una instancia de esta clase como una fuente de datos a uno de[`ReportingEngine`](../reportingengine/) .BuildReport sobrecargas.

En documentos de plantilla, si un elemento JSON de nivel superior es una matriz, un`JsonDataSource` La instancia debe ser tratada de la misma manera que si fuera unDataTable instancia. Si un elemento JSON de nivel superior es un objeto, un`JsonDataSource` La instancia debe tratarse de la misma manera que si fuera unDataRow instancia. Para obtener más información, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

En documentos de plantilla, puede trabajar con valores escritos de elementos JSON. Para mayor comodidad, el motor reemplaza el conjunto de tipos simples JSON por el siguiente:

* Nullable
* Nullable
* Nullable
* Nullable
* String

El motor reconoce automáticamente los valores de los tipos adicionales en sus representaciones JSON.

Para anular el comportamiento predeterminado de la carga de datos JSON, inicialice y pase un[`JsonDataLoadOptions`](../jsondataloadoptions/) instancia a un constructor de esta clase.

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)


