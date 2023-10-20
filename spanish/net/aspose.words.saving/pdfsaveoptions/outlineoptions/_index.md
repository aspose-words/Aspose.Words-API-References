---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words para .NET
description: PdfSaveOptions OutlineOptions propiedad. Permite especificar opciones de contorno en C#.
type: docs
weight: 240
url: /es/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Permite especificar opciones de contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Observaciones

Se pueden crear esquemas a partir de encabezados y marcadores.

Para los títulos, el nivel del esquema está determinado por el nivel del título.

Es posible establecer el nivel máximo de encabezado para incluirlo en los esquemas o desactivarlos por completo.

Para los marcadores, el nivel de esquema se puede configurar en las opciones como un valor predeterminado para todos los marcadores o como valores individuales para marcadores particulares.

Además, los esquemas se pueden exportar al formato XPS utilizando el mismo`OutlineOptions` clase.

## Ejemplos

Muestra cómo limitar el nivel de los títulos que aparecerán en el esquema de un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas TOC de los niveles 1, 2 y luego 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los títulos en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "2" para excluir del esquema todos los encabezados cuyos niveles estén por encima de 2.
// Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Muestra cómo trabajar con niveles de esquema que no contienen ningún encabezado correspondiente al guardar un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar títulos que puedan servir como entradas TOC de los niveles 1 y 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los títulos en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "5" para incluir todos los títulos de los niveles 5 e inferiores en el esquema.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Este documento contiene títulos de niveles 1 y 5, y ningún título con niveles de 2, 3 y 4.
// El documento PDF de salida considerará que "faltan" los niveles de esquema 2, 3 y 4.
// Establece la propiedad "CreateMissingOutlineLevels" en "true" para incluir todos los niveles que faltan en el esquema,
// dejando entradas de esquema en blanco ya que no hay encabezados utilizables.
// Establece la propiedad "CreateMissingOutlineLevels" en "false" para ignorar los niveles de esquema que faltan,
// y trate los encabezados del nivel 5 del esquema como de nivel 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ver también

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
