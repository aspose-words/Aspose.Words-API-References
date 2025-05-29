---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words para .NET
description: Genere sin esfuerzo informes listos para usar con el método BuildReport de ReportingEngine, completando sin problemas las plantillas con datos de la fuente elegida.
type: docs
weight: 50
url: /es/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSource | Object | Un objeto de fuente de datos. |

### Valor_devuelto

Una bandera que indica si el análisis del documento de plantilla fue exitoso. La bandera devuelta solo tiene sentido si un valor de la[`Options`](../options/) La propiedad incluye elInlineErrorMessages opción.

## Observaciones

Con esta sobrecarga, puede referenciar los miembros de la fuente de datos en el documento de plantilla, pero no puede referenciar el objeto de la fuente de datos en sí. Debe usar`BuildReport` sobrecarga para lograr esto.

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
* Cualquier otro tipo .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Rellena el documento de plantilla especificado con datos de la fuente especificada, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSource | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |

### Valor_devuelto

Una bandera que indica si el análisis del documento de plantilla fue exitoso. La bandera devuelta solo tiene sentido si un valor de la[`Options`](../options/) La propiedad incluye elInlineErrorMessages opción.

## Observaciones

Con esta sobrecarga, puede hacer referencia a los miembros de la fuente de datos y al objeto de la fuente de datos en la plantilla. Si no va a hacer referencia al objeto de la fuente de datos en sí, puede omitir*dataSourceName* pasando`nulo` o utiliza el`BuildReport` sobrecarga.

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
* Cualquier otro tipo .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Ejemplos

Muestra cómo permitir miembros faltantes.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Muestra cómo eliminar párrafos de forma selectiva.

```csharp
La plantilla contiene etiquetas con un signo de exclamación. Para estas etiquetas, se eliminarán los párrafos vacíos.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Muestra cómo mostrar valores como texto en dólares.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Rellena el documento de plantilla especificado con datos de las fuentes especificadas, convirtiéndolo en un informe listo.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| document | Document | Un documento de plantilla que se rellenará con datos. |
| dataSources | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |

### Valor_devuelto

Una bandera que indica si el análisis del documento de plantilla fue exitoso. La bandera devuelta solo tiene sentido si un valor de la[`Options`](../options/) La propiedad incluye elInlineErrorMessages opción.

## Observaciones

Con esta sobrecarga, puede hacer referencia a varios objetos de origen de datos y sus miembros en la plantilla. El nombre del primer origen de datos se puede omitir (es decir, puede ser una cadena vacía o`nulo` si va a hacer referencia a los miembros de la fuente de datos, pero no al objeto de la fuente de datos en sí. Los nombres de las otras fuentes de datos deben especificarse y ser únicos.

Si va a utilizar una única fuente de datos, considere utilizar de`BuildReport` y`BuildReport` sobrecargas en su lugar.

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
* Cualquier otro tipo .NET arbitrario no dinámico y no anónimo

Para obtener información sobre cómo trabajar con fuentes de datos de diferentes tipos en documentos de plantilla, consulte la referencia de sintaxis de plantilla (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Ejemplos

Muestra cómo trabajar con gráficos de Word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Muestra cómo mantener la numeración insertada tal como está.

```csharp
// De forma predeterminada, las listas numeradas de un documento de plantilla continúan cuando sus identificadores coinciden con los de un documento que se está insertando.
// Con "-sourceNumbering" la numeración debe separarse y mantenerse como está.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
