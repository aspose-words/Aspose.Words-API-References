---
title: OutlineOptions.HeadingsOutlineLevels
second_title: Referencia de API de Aspose.Words para .NET
description: OutlineOptions propiedad. Especifica cuántos niveles de encabezados párrafos formateados con los estilos de encabezado para incluir en el esquema del documento .
type: docs
weight: 70
url: /es/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

Especifica cuántos niveles de encabezados (párrafos formateados con los estilos de encabezado) para incluir en el esquema del documento .

```csharp
public int HeadingsOutlineLevels { get; set; }
```

### Observaciones

Especifique 0 para que no haya encabezados en el esquema; especifique 1 para un nivel de encabezados en el esquema y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

### Ejemplos

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados de niveles 1 a 5.
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

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su respectivo encabezado.
// Establezca la propiedad "HeadingsOutlineLevels" en "4" para excluir todos los encabezados cuyos niveles estén por encima de 4 del esquema.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si una entrada de esquema tiene entradas posteriores de un nivel superior entre ella y la siguiente entrada del mismo nivel o inferior,
// aparecerá una flecha a la izquierda de la entrada. Esta entrada es el "propietario" de varias de estas "subentradas".
// En nuestro documento, las entradas de esquema del 5.º nivel de encabezado son subentradas de la segunda entrada de esquema del 4.º nivel,
  // las entradas de nivel de encabezado 4 y 5 son subentradas de la segunda entrada de nivel 3, y así sucesivamente.
// En el esquema, podemos hacer clic en la flecha de la entrada "propietario" para colapsar/expandir todas sus subentradas.
// Establezca la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de encabezado de nivel 2 e inferior
 // y colapsar todas las entradas de nivel y 3 y superiores cuando abrimos el documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../outlineoptions/)
* asamblea [Aspose.Words](../../../)


