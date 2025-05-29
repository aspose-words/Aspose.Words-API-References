---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words para .NET
description: Elimina fácilmente las tabulaciones de tu colección con el método RemoveByPosition. Optimiza el formato para un mejor control de tus documentos.
type: docs
weight: 120
url: /es/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Elimina una tabulación en la posición especificada de la colección.

```csharp
public void RemoveByPosition(double position)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| position | Double | La posición (en puntos) de la tabulación que se va a quitar. |

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

* class [TabStopCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
