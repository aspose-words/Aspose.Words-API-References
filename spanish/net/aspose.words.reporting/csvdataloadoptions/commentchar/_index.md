---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar la propiedad CommentChar en CsvDataLoadOptions para optimizar la gestión de datos CSV. ¡Optimice la carga de datos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

Obtiene o establece el carácter que se utiliza para comentar líneas de datos CSV.

```csharp
public char CommentChar { get; set; }
```

## Observaciones

El valor predeterminado es '#' (signo de número).

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
