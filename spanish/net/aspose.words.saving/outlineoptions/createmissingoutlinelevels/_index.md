---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad CreateMissingOutlineLevels en OutlineOptions mejora las exportaciones de documentos al generar automáticamente niveles de esquema faltantes para una mejor organización.
type: docs
weight: 30
url: /es/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Obtiene o establece un valor que determina si se deben crear o no niveles de contorno faltantes cuando se exporta el documento.

El valor predeterminado para esta propiedad es`FALSO`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Ejemplos

Muestra cómo trabajar con niveles de esquema que no contienen ningún encabezado correspondiente al guardar un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas TOC de los niveles 1 y 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "5" para incluir todos los encabezados de niveles 5 e inferiores en el esquema.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Este documento contiene encabezados de niveles 1 y 5, y ningún encabezado con niveles 2, 3 y 4.
// El documento PDF de salida tratará los niveles de esquema 2, 3 y 4 como "faltantes".
// Establezca la propiedad "CreateMissingOutlineLevels" en "true" para incluir todos los niveles faltantes en el esquema,
// dejando entradas de esquema en blanco ya que no hay encabezados utilizables.
// Establezca la propiedad "CreateMissingOutlineLevels" en "falso" para ignorar los niveles de contorno faltantes,
// y tratar los encabezados de nivel 5 del esquema como de nivel 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
