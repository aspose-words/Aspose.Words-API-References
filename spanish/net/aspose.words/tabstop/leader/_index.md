---
title: TabStop.Leader
second_title: Referencia de API de Aspose.Words para .NET
description: TabStop propiedad. Obtiene o establece el tipo de línea guía que se muestra bajo el carácter de tabulación.
type: docs
weight: 40
url: /es/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Obtiene o establece el tipo de línea guía que se muestra bajo el carácter de tabulación.

```csharp
public TabLeader Leader { get; set; }
```

### Ejemplos

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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* espacio de nombres [Aspose.Words](../../tabstop/)
* asamblea [Aspose.Words](../../../)


