---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words para .NET
description: Descubre la propiedad PageSetup LayoutMode para personalizar fácilmente el diseño de tu documento. ¡Mejora tu diseño con opciones flexibles de sección!
type: docs
weight: 190
url: /es/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Obtiene o establece el modo de diseño de esta sección.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

## Ejemplos

Muestra cómo especificar la cantidad de caracteres que puede tener cada línea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el paso y luego úselo para establecer la cantidad de caracteres por línea en esta sección.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

//El número de caracteres también depende del tamaño de la fuente.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Muestra cómo especificar un límite para la cantidad de líneas que puede tener cada página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el paso y luego úselo para establecer la cantidad de líneas por página en esta sección.
// Un tamaño de fuente lo suficientemente grande empujará algunas líneas hacia la página siguiente para evitar superponer caracteres.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Ver también

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
