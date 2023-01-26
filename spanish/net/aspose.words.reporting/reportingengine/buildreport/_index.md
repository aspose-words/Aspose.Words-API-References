---
title: BuildReport
second_title: Referencia de API de Aspose.Words para .NET
description: Rellena el documento de plantilla especificado con datos de la fuente especificada convirtiéndolo en un informe listo.
type: docs
weight: 40
url: /es/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Rellena el documento de plantilla especificado con datos de la fuente especificada convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se completará con datos. |
| dataSource | Object | Un objeto de origen de datos. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto tiene sentido solo si un valor del[`Options`](../options/)propiedad incluye elInlineErrorMessages opción.

### Observaciones

Con esta sobrecarga, puede hacer referencia a los miembros del origen de datos en el documento de plantilla, pero no puede hacer referencia al objeto de origen de datos en sí. Deberías usar el`BuildReport` sobrecarga para lograr esto.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Cualquier otro tipo de .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../reportingengine/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Rellena el documento de plantilla especificado con datos de la fuente especificada convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se completará con datos. |
| dataSource | Object | Un objeto de origen de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de origen de datos en la plantilla. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto tiene sentido solo si un valor del[`Options`](../options/)propiedad incluye elInlineErrorMessages opción.

### Observaciones

Con esta sobrecarga, puede hacer referencia a los miembros de la fuente de datos y al propio objeto de la fuente de datos en la plantilla. Si no va a hacer referencia al objeto de fuente de datos en sí, puede omitir*dataSourceName* pasando nulo o usa el`BuildReport` sobrecarga.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Cualquier otro tipo de .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../reportingengine/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Rellena el documento de plantilla especificado con datos de las fuentes especificadas convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se completará con datos. |
| dataSources | Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de origen de datos dentro de la plantilla. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto tiene sentido solo si un valor del[`Options`](../options/)propiedad incluye elInlineErrorMessages opción.

### Observaciones

Con esta sobrecarga, puede hacer referencia a varios objetos de origen de datos y sus miembros en la plantilla. El nombre de la primera fuente de datos se puede omitir (es decir, puede ser una cadena vacía o nula) si va a hacer referencia a los miembros de la fuente de datos pero no al objeto de la fuente de datos en sí. Los nombres de las otras fuentes de datos deben especificarse y ser únicos.

Si va a usar una sola fuente de datos, considere usar de`BuildReport` y`BuildReport` sobrecarga en su lugar.

Un objeto de fuente de datos puede ser de uno de los siguientes tipos:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Cualquier otro tipo de .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../reportingengine/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
