---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageNumberStyle de PageSetup para personalizar fácilmente el formato de número de página para mejorar la presentación y claridad del documento.
type: docs
weight: 320
url: /es/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

Obtiene o establece el formato del número de página.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## Ejemplos

Muestra cómo configurar la numeración de páginas en una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Mueva el generador de documentos al encabezado principal de la primera sección,
// que se mostrará en cada página de esa sección.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserta un campo PÁGINA, que mostrará el número de la página actual.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configure la sección para que el recuento de páginas que muestran los campos PÁGINA comience desde 5.
// Además, configure todos los campos PÁGINA para mostrar sus números de página utilizando números romanos en mayúsculas.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Crea otro encabezado principal para la segunda sección, con otro campo PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configure la sección para que el recuento de páginas que muestran los campos PÁGINA comience desde 10.
// Además, configure todos los campos PÁGINA para mostrar sus números de página utilizando números arábigos.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Ver también

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
