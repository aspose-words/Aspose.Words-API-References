---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words para .NET
description: PageSetup BorderSurroundsHeader propiedad. Especifica si el borde de la página incluye o excluye el encabezado en C#.
type: docs
weight: 70
url: /es/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Especifica si el borde de la página incluye o excluye el encabezado.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Observaciones

Nota: cambiar esta propiedad afecta a todas las secciones del documento.

## Ejemplos

Muestra cómo aplicar un borde a la página y al encabezado/pie de página.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Inserta un borde azul de doble línea.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// El objeto PageSetup de una sección tiene los indicadores "BorderSurroundsHeader" y "BorderSurroundsFooter" que determinan
// si un borde de página rodea el texto del cuerpo principal, también incluye el encabezado o pie de página, respectivamente.
// Establece el indicador "BorderSurroundsHeader" en "true" para rodear el encabezado con nuestro borde,
// y luego configura el indicador "BorderSurroundsFooter" para dejar el pie de página fuera del borde.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
