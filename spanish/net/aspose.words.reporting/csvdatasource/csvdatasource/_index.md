---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: Aspose.Words para .NET
description: Cree fácilmente una potente fuente de datos CSV con nuestro constructor CsvDataSource. Simplifique el análisis de datos con opciones predeterminadas para una integración perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones predeterminadas para analizar datos CSV.

```csharp
public CsvDataSource(string csvPath)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| csvPath | String | La ruta al archivo CSV que se utilizará como fuente de datos. |

### Ver también

* class [CsvDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

Crea una nueva fuente de datos con datos de un archivo CSV utilizando las opciones especificadas para analizar datos CSV.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| csvPath | String | La ruta al archivo CSV que se utilizará como fuente de datos. |
| options | CsvDataLoadOptions | Opciones para analizar los datos CSV. |

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

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

Crea una nueva fuente de datos con datos de una secuencia CSV utilizando las opciones predeterminadas para analizar datos CSV.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| csvStream | Stream | El flujo de datos CSV que se utilizará como fuente de datos. |

### Ver también

* class [CsvDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

Crea una nueva fuente de datos con datos de una secuencia CSV utilizando las opciones especificadas para analizar datos CSV.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| csvStream | Stream | El flujo de datos CSV que se utilizará como fuente de datos. |
| options | CsvDataLoadOptions | Opciones para analizar los datos CSV. |

## Ejemplos

Muestra cómo utilizar CSV como fuente de datos (transmisión).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Ver también

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
