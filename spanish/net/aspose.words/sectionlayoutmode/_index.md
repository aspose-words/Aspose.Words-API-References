---
title: Enum SectionLayoutMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.SectionLayoutMode enumeración. Especifica el modo de diseño de una sección que permite definir el comportamiento de la cuadrícula del documento.
type: docs
weight: 5750
url: /es/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Especifica el modo de diseño de una sección que permite definir el comportamiento de la cuadrícula del documento.

```csharp
public enum SectionLayoutMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Especifica que no se aplicará ninguna cuadrícula de documento al contenido de la sección correspondiente del documento. |
| Grid | `1` | Especifica que a la sección correspondiente se le agregará el paso de línea adicional y el paso de carácter a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres no se alinearán automáticamente con las líneas de la cuadrícula en escribiendo. |
| LineGrid | `2` | Especifica que a la sección correspondiente se le agregará un paso de línea adicional a cada línea dentro de ella para mantener el número especificado de líneas por página. |
| SnapToChars | `3` | Especifica que a la sección correspondiente se le agregará el paso de línea adicional y el paso de carácter a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres se alinearán automáticamente con las líneas de la cuadrícula al escribir. |

### Ejemplos

Muestra cómo especificar un para el número de caracteres que puede tener cada línea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el paso y luego utilícelo para establecer el número de caracteres por línea en esta sección.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// El número de caracteres también depende del tamaño de la fuente.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Muestra cómo especificar un límite para el número de líneas que puede tener cada página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el lanzamiento y luego utilícelo para establecer el número de líneas por página en esta sección.
// Un tamaño de fuente lo suficientemente grande empujará algunas líneas hacia la página siguiente para evitar la superposición de caracteres.
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


