---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words para .NET
description: Explore la propiedad PageSetup de DocumentBuilder para acceder a la configuración de página y sección actual, mejorando así el formato de su documento y la eficiencia del diseño.
type: docs
weight: 160
url: /es/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Devuelve un objeto que representa la configuración de la página actual y las propiedades de la sección.

```csharp
public PageSetup PageSetup { get; }
```

## Ejemplos

Muestra cómo aplicar y revertir configuraciones de configuración de página a secciones de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifique las propiedades de configuración de la página para la sección actual del constructor y agregue texto.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Si comenzamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actual del constructor.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

//Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ver también

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
