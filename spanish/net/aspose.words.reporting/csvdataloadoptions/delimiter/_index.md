---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: Aspose.Words para .NET
description: Descubra la propiedad Delimitador CsvDataLoadOptions para personalizar fácilmente los delimitadores de columnas y optimizar la carga de datos. ¡Optimice su gestión de datos hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Obtiene o establece el carácter que se utilizará como delimitador de columna.

```csharp
public char Delimiter { get; set; }
```

## Observaciones

El valor predeterminado es "," (coma).

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

* class [CsvDataLoadOptions](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
