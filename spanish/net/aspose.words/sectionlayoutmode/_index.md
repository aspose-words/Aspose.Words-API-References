---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.SectionLayoutMode para optimizar los diseños de secciones y mejorar el comportamiento de la cuadrícula del documento para un mejor control del formato.
type: docs
weight: 6580
url: /es/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Especifica el modo de diseño para una sección que permite definir el comportamiento de la cuadrícula del documento.

```csharp
public enum SectionLayoutMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Especifica que no se aplicará ninguna cuadrícula de documento al contenido de la sección correspondiente en el documento. |
| Grid | `1` | Especifica que la sección correspondiente tendrá tanto el paso de línea adicional como el paso de carácter agregados a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres no se alinearán automáticamente con las líneas de cuadrícula al escribir. |
| LineGrid | `2` | Especifica que se debe agregar un paso de línea adicional a cada línea dentro de la sección correspondiente para mantener la cantidad especificada de líneas por página. |
| SnapToChars | `3` | Especifica que la sección correspondiente tendrá tanto el paso de línea adicional como el paso de carácter agregados a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres se alinearán automáticamente con las líneas de cuadrícula al escribir. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
