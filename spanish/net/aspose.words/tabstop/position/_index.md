---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: Descubra la propiedad Posición de tabulación para encontrar fácilmente las ubicaciones de las tabulaciones en los puntos, mejorando así la precisión y la eficiencia del diseño.
type: docs
weight: 50
url: /es/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Obtiene la posición de la tabulación en puntos.

```csharp
public double Position { get; }
```

## Ejemplos

Muestra cómo modificar la posición de la tabulación derecha en los párrafos relacionados con la tabla de contenidos.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterar a través de todos los párrafos con estilos basados en resultados de TOC; este es cualquier estilo entre TOC y TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Obtenga la primera tabulación utilizada en este párrafo, ésta debe ser la tabulación utilizada para alinear los números de página.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Reemplace la primera tabulación predeterminada con una tabulación personalizada.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ver también

* class [TabStop](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
