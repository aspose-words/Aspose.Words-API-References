---
title: PageSetup.Orientation
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Devuelve o establece la orientación de la página.
type: docs
weight: 280
url: /es/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

Devuelve o establece la orientación de la página.

```csharp
public Orientation Orientation { get; set; }
```

### Observaciones

Cambiando **Orientación** permutas[`PageWidth`](../pagewidth/) y[`PageHeight`](../pageheight/).

### Ejemplos

Muestra cómo ajustar el tamaño del papel, la orientación, los márgenes y otras configuraciones para una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Muestra cómo aplicar y revertir la configuración de configuración de página a las secciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifique las propiedades de configuración de la página para la sección actual del constructor y agregue texto.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si comenzamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de la página actual del constructor.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ver también

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


