---
title: OutlineOptions.HeadingsOutlineLevels
linktitle: HeadingsOutlineLevels
articleTitle: HeadingsOutlineLevels
second_title: Aspose.Words para .NET
description: Descubra la propiedad HeadingsOutlineLevels en OutlineOptions. Controle los niveles de encabezado de documentos estructurados y facilite la navegación.
type: docs
weight: 70
url: /es/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

Especifica cuántos niveles de encabezados (párrafos formateados con los estilos de encabezado) se incluirán en el esquema del documento.

```csharp
public int HeadingsOutlineLevels { get; set; }
```

## Observaciones

Especifique 0 para no haber encabezados en el esquema; especifique 1 para un nivel de encabezados en el esquema y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

## Ejemplos

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados de niveles 1 al 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema accederemos a la ubicación de su encabezado respectivo.
// Establezca la propiedad "HeadingsOutlineLevels" en "4" para excluir del esquema todos los encabezados cuyos niveles sean superiores a 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si una entrada de esquema tiene entradas subsiguientes de un nivel superior entre ella y la siguiente entrada del mismo nivel o de un nivel inferior,
Aparecerá una flecha a la izquierda de la entrada. Esta entrada es la "propietaria" de varias subentradas similares.
// En nuestro documento, las entradas del esquema del quinto nivel de encabezado son subentradas de la segunda entrada del esquema del cuarto nivel.
// las entradas de nivel de encabezado 4º y 5º son subentradas de la segunda entrada de nivel 3, y así sucesivamente.
// En el esquema, podemos hacer clic en la flecha de la entrada "propietario" para contraer/expandir todas sus subentradas.
// Establezca la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de encabezado de nivel 2 y de esquema inferior
// y colapsar todas las entradas de nivel 3 y superiores cuando abrimos el documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
