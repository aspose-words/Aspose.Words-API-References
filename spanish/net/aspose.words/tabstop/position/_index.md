---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words para .NET
description: TabStop Position propiedad. Obtiene la posición de la tabulación en puntos en C#.
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

Muestra cómo modificar la posición de la tabulación derecha en párrafos relacionados con TOC.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterar a través de todos los párrafos con estilos basados en resultados TOC; este es cualquier estilo entre TOC y TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Obtenga la primera pestaña utilizada en este párrafo, esta debería ser la pestaña utilizada para alinear los números de página.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Reemplace la primera pestaña predeterminada, deténgase con una tabulación personalizada.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ver también

* class [TabStop](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
