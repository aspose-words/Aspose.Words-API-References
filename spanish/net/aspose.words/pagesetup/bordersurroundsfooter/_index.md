---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PageSetup BorderSurroundsFooter puede mejorar el diseño de su documento al controlar la inclusión del pie de página en los bordes de la página.
type: docs
weight: 60
url: /es/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Especifica si el borde de la página incluye o excluye el pie de página.

```csharp
public bool BorderSurroundsFooter { get; set; }
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

// Insertar un borde de doble línea azul.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// El objeto PageSetup de una sección tiene indicadores "BorderSurroundsHeader" y "BorderSurroundsFooter" que determinan
// si un borde de página rodea el texto del cuerpo principal, también incluye el encabezado o pie de página, respectivamente.
// Establezca el indicador "BorderSurroundsHeader" en "verdadero" para rodear el encabezado con nuestro borde,
// y luego configure el indicador "BorderSurroundsFooter" para dejar el pie de página fuera del borde.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
