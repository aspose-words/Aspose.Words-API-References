---
title: ParagraphFormat.SnapToGrid
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Especifica si el párrafo actual debe utilizar las líneas de la cuadrícula del documento por configuración de página al diseñar el contenido del párrafo.
type: docs
weight: 290
url: /es/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Especifica si el párrafo actual debe utilizar las líneas de la cuadrícula del documento por configuración de página al diseñar el contenido del párrafo.

```csharp
public bool SnapToGrid { get; set; }
```

### Ejemplos

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

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


