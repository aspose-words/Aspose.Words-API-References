---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SnapToGrid de ParagraphFormat mejora la precisión del diseño al alinear sus párrafos con las líneas de la cuadrícula del documento para lograr una apariencia pulida.
type: docs
weight: 300
url: /es/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Especifica si el párrafo actual debe utilizar la configuración de líneas de cuadrícula por página del documento al diseñar el contenido en el párrafo.

```csharp
public bool SnapToGrid { get; set; }
```

## Ejemplos

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

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
