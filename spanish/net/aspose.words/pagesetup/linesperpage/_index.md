---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words para .NET
description: PageSetup LinesPerPage propiedad. Obtiene o establece el número de líneas por página en la cuadrícula del documento en C#.
type: docs
weight: 240
url: /es/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Obtiene o establece el número de líneas por página en la cuadrícula del documento.

```csharp
public int LinesPerPage { get; set; }
```

## Observaciones

El valor mínimo de la propiedad es 1. El valor máximo depende de la altura de la página y el tamaño de fuente del estilo Normal . El paso mínimo de línea es el 136 por ciento del tamaño de fuente. Por ejemplo, el número máximo de líneas por página de una página Carta con márgenes de una pulgada es 39.

De forma predeterminada, la propiedad tiene un valor en el que el paso de línea es 1,5 veces mayor que el tamaño de fuente de el estilo Normal.

## Ejemplos

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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
