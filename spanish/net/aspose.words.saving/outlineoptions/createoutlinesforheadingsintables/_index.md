---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad CreateOutlinesForHeadingsInTables mejora la organización de la tabla al habilitar esquemas para estilos de encabezado, mejorando así la claridad del documento.
type: docs
weight: 40
url: /es/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Especifica si se deben crear o no esquemas para encabezados (párrafos formateados con los estilos de encabezado) dentro de las tablas.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO`.

## Ejemplos

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

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "1" para obtener el esquema
// para registrar únicamente encabezados con niveles de encabezado que no sean mayores a 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Establezca la propiedad "CreateOutlinesForHeadingsInTables" en "falso" para excluir todos los encabezados dentro de las tablas,
// como el que hemos creado arriba a partir del esquema.
// Establezca la propiedad "CreateOutlinesForHeadingsInTables" en "verdadero" para incluir todos los encabezados dentro de las tablas
// en el esquema, siempre que tengan un nivel de encabezado que no sea mayor que el valor de la propiedad "HeadingsOutlineLevels".
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
