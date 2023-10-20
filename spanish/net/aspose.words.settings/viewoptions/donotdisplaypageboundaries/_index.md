---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words para .NET
description: ViewOptions DoNotDisplayPageBoundaries propiedad. Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página en C#.
type: docs
weight: 20
url: /es/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Desactiva la visualización del espacio entre la parte superior del texto y el borde superior de la página.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Ejemplos

Muestra cómo ocultar espacios en blanco verticales y encabezados/pies de página en las opciones de visualización.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta contenido que abarque 3 páginas.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Insertar un encabezado y un pie de página.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Este documento contiene una pequeña cantidad de contenido que ocupa unas pocas páginas completas de espacio.
// Establece el indicador "DoNotDisplayPageBoundaries" en "true" para que las versiones anteriores de Microsoft Word omitan los encabezados.
// pies de página y gran parte de los espacios en blanco verticales al mostrar nuestro documento.
// Establece el indicador "DoNotDisplayPageBoundaries" en "false" para obtener versiones anteriores de Microsoft Word
// para mostrar normalmente nuestro documento.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Ver también

* class [ViewOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
