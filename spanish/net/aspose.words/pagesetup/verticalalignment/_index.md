---
title: PageSetup.VerticalAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Devuelve o establece la alineación vertical del texto en cada página de un documento o sección.
type: docs
weight: 450
url: /es/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Devuelve o establece la alineación vertical del texto en cada página de un documento o sección.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

### Ejemplos

Muestra cómo aplicar y revertir la configuración de configuración de página a secciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica las propiedades de configuración de la página para la sección actual del constructor y agrega texto.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si comenzamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actual del constructor.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Podemos revertir las propiedades de configuración de la página a sus valores predeterminados usando el método "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ver también

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


