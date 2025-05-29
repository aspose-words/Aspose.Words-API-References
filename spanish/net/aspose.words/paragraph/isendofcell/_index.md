---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsEndOfCell para párrafos. Aprenda a identificar si un párrafo es el último de una celda, mejorando así la estructura de su documento.
type: docs
weight: 50
url: /es/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Verdadero si este párrafo es el último párrafo de un[`Cell`](../../../aspose.words.tables/cell/) ; falso en caso contrario.

```csharp
public bool IsEndOfCell { get; }
```

## Ejemplos

Muestra cómo preparar una mesa para permanecer juntos en la misma página.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Habilitar KeepWithNext para cada párrafo de la tabla excepto el
// Los últimos en la última fila evitarán que la tabla se divida en varias páginas.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
