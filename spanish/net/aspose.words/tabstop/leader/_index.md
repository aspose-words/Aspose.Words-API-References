---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words para .NET
description: Descubra las propiedades de TabStop Leader para personalizar los tipos de líneas guía para sus tabulaciones, mejorando la claridad y la presentación del documento. ¡Optimice su formato hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Obtiene o establece el tipo de línea guía que se muestra debajo del carácter de tabulación.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
