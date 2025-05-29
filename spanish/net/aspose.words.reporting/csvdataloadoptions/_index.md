---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Reporting.CsvDataLoadOptions para un análisis eficiente de datos CSV. ¡Optimice el procesamiento de sus documentos con opciones personalizables hoy mismo!
type: docs
weight: 5400
url: /es/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

Representa opciones para analizar datos CSV.

Para obtener más información, visite el[Motor de informes LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) Artículo de documentación.

```csharp
public class CsvDataLoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Inicializa una nueva instancia de esta clase con opciones predeterminadas. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | Inicializa una nueva instancia de esta clase especificando si los datos CSV contienen nombres de columna en la primera línea. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | Obtiene o establece el carácter que se utiliza para comentar líneas de datos CSV. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Obtiene o establece el carácter que se utilizará como delimitador de columna. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | Obtiene o establece un valor que indica si el primer registro de datos CSV contiene nombres de columnas. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Obtiene o establece el carácter que se utiliza para citar valores de campo. |

## Observaciones

Se puede pasar una instancia de esta clase a los constructores de[`CsvDataSource`](../csvdatasource/) .

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
