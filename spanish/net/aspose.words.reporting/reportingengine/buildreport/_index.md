---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words para .NET
description: ReportingEngine BuildReport método. Completa el documento de plantilla especificado con datos de la fuente especificada convirtiéndolo en un informe listo en C#.
type: docs
weight: 40
url: /es/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Completa el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSource | Object | Un objeto de origen de datos. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto sólo tiene sentido si un valor del[`Options`](../options/)la propiedad incluye elInlineErrorMessages opción.

## Observaciones

Al utilizar esta sobrecarga, puede hacer referencia a los miembros de la fuente de datos en el documento de plantilla, pero no puede hacer referencia al objeto de la fuente de datos en sí. Deberías usar el`BuildReport` sobrecarga para lograr esto.

Un objeto de origen de datos puede ser de uno de los siguientes tipos:

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
* Cualquier otro tipo .NET arbitrario, no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Completa el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSource | Object | Un objeto de origen de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de origen de datos en la plantilla. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto sólo tiene sentido si un valor del[`Options`](../options/)la propiedad incluye elInlineErrorMessages opción.

## Observaciones

Al utilizar esta sobrecarga, puede hacer referencia a los miembros de la fuente de datos y al propio objeto de la fuente de datos en la plantilla. Si no va a hacer referencia al objeto de fuente de datos en sí, puede omitir*dataSourceName* pasando`nulo` o utilizar el`BuildReport` sobrecarga.

Un objeto de origen de datos puede ser de uno de los siguientes tipos:

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
* Cualquier otro tipo .NET arbitrario, no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Completa el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSources | Object[] | Una matriz de objetos de origen de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de origen de datos dentro de la plantilla. |

### Valor_devuelto

Un indicador que indica si el análisis del documento de plantilla fue exitoso. El indicador devuelto sólo tiene sentido si un valor del[`Options`](../options/)la propiedad incluye elInlineErrorMessages opción.

## Observaciones

Con esta sobrecarga puede hacer referencia a múltiples objetos de origen de datos y sus miembros en la plantilla. El nombre de la primera fuente de datos se puede omitir (es decir, ser una cadena vacía o`nulo` si va a hacer referencia a los miembros de la fuente de datos pero no al objeto de la fuente de datos en sí. Los nombres de las otras fuentes de datos deben ser especificados y únicos.

Si va a utilizar una única fuente de datos, considere usar`BuildReport` y`BuildReport` sobrecargas en su lugar.

Un objeto de origen de datos puede ser de uno de los siguientes tipos:

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
* Cualquier otro tipo .NET arbitrario, no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
