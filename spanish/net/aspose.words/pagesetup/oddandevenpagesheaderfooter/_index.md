---
title: PageSetup.OddAndEvenPagesHeaderFooter
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Verdadero si el documento tiene diferentes encabezados y pies de página para páginas pares e impares.
type: docs
weight: 280
url: /es/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Verdadero si el documento tiene diferentes encabezados y pies de página para páginas pares e impares.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

### Observaciones

Nota: cambiar esta propiedad afecta a todas las secciones del documento.

### Ejemplos

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especifica que queremos encabezados y pies de página diferentes para las primeras páginas, pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados, luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Muestra cómo habilitar o deshabilitar incluso encabezados/pies de página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos tipos de encabezados/pies de página.
// 1 - El encabezado/pie de página "Principal", que aparece en cada página de la sección.
 // Podemos anular el encabezado/pie de página principal por un encabezado/pie de página primero y par.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - El encabezado/pie de página "Par", que aparece en cada página par de esta sección.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Cada sección tiene un objeto "PageSetup" que especifica las propiedades relacionadas con la apariencia de la página
// como orientación, tamaño y bordes.
// Establece la propiedad "OddAndEvenPagesHeaderFooter" en "verdadero"
// para mostrar el encabezado/pie de página de las páginas pares.
// Establece la propiedad "OddAndEvenPagesHeaderFooter" en "falso"
// para mostrar el encabezado/pie de página principal en páginas pares.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


