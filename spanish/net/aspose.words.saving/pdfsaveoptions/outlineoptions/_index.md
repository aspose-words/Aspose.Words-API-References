---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words para .NET
description: Descubre la propiedad OutlineOptions de PdfSaveOptions para personalizar fácilmente los contornos de tus PDF. ¡Mejora la navegación y la usabilidad de tus documentos!
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

Para los encabezados, el nivel del esquema está determinado por el nivel del encabezado.

Es posible establecer el nivel de encabezado máximo que se incluirá en los contornos o deshabilitar los contornos de encabezado por completo.

Para los marcadores, el nivel de esquema se puede configurar en las opciones como un valor predeterminado para todos los marcadores o como valores individuales para marcadores particulares.

Además, los contornos se pueden exportar al formato XPS utilizando el mismo`OutlineOptions` clase.

## Ejemplos

Muestra cómo limitar el nivel de encabezados que aparecerán en el esquema de un documento PDF guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados que puedan servir como entradas de TOC de los niveles 1, 2 y luego 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir del esquema todos los encabezados cuyos niveles sean superiores a 2.
//Los dos últimos encabezados que hemos insertado arriba no aparecerán.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

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

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
