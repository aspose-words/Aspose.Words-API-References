---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
second_title: Referencia de API de Aspose.Words para .NET
description: OutlineOptions propiedad. Especifica si se crean o no esquemas para los encabezados párrafos formateados con estilos de encabezado dentro de las tablas.
type: docs
weight: 40
url: /es/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Especifica si se crean o no esquemas para los encabezados (párrafos formateados con estilos de encabezado) dentro de las tablas.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO`.

### Ejemplos

Muestra cómo crear entradas de esquema de documentos PDF para encabezados dentro de tablas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabla con tres filas. La primera fila,
// cuyo texto formatearemos en un estilo de tipo encabezado, servirá como encabezado de columna.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los títulos en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "1" para obtener el esquema
// para registrar solo encabezados con niveles de encabezado que no sean mayores que 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Establece la propiedad "CreateOutlinesForHeadingsInTables" en "false" para excluir todos los encabezados dentro de las tablas.
// como el que hemos creado arriba a partir del esquema.
// Establece la propiedad "CreateOutlinesForHeadingsInTables" en "true" para incluir todos los encabezados dentro de las tablas
// en el esquema, siempre que tengan un nivel de encabezado que no sea mayor que el valor de la propiedad "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../outlineoptions/)
* asamblea [Aspose.Words](../../../)


