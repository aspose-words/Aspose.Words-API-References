---
title: MailMergeSettings.HeaderSource
second_title: Referencia de API de Aspose.Words para .NET
description: MailMergeSettings propiedad. Especifica la ruta al origen del encabezado de combinación de correspondencia. El valor predeterminado es una cadena vacía.
type: docs
weight: 100
url: /es/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

Especifica la ruta al origen del encabezado de combinación de correspondencia. El valor predeterminado es una cadena vacía.

```csharp
public string HeaderSource { get; set; }
```

### Ejemplos

Muestra cómo construir una fuente de datos para una combinación de correspondencia a partir de una fuente de encabezado y una fuente de datos.

```csharp
// Cree un archivo de encabezado de combinación de etiquetas de correo, que constará de una tabla con una fila.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// Crea un archivo de datos de combinación de etiquetas de correo que consta de una tabla con una fila
 // y el mismo número de columnas que la tabla del documento de encabezado.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// Crea un documento de destino de fusión con MERGEFIELDS con nombres que
// coincide con los nombres de las columnas en la tabla del archivo de encabezado de combinación.
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// Construya una fuente de datos para nuestra combinación de correspondencia especificando dos nombres de archivo de documentos.
// La fuente del encabezado nombrará las columnas de la tabla de fuente de datos.
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// La fuente de datos proporcionará filas de datos para todas las columnas de la tabla del documento de encabezado.
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// Configurar una combinación de correspondencia de tipo etiqueta de correo, que Microsoft Word ejecutará
// tan pronto como lo usemos para cargar el documento de salida.
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### Ver también

* class [MailMergeSettings](../)
* espacio de nombres [Aspose.Words.Settings](../../mailmergesettings/)
* asamblea [Aspose.Words](../../../)


