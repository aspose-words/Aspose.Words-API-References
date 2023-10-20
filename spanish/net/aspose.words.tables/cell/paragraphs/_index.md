---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words para .NET
description: Cell Paragraphs propiedad. Obtiene una colección de párrafos que son hijos inmediatos de la celda en C#.
type: docs
weight: 90
url: /es/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Obtiene una colección de párrafos que son hijos inmediatos de la celda.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Ejemplos

Muestra cómo configurar una mesa para que permanezcan juntas en la misma página.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Habilitando KeepWithNext para cada párrafo de la tabla excepto el
// los últimos en la última fila evitarán que la tabla se divida en varias páginas.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Ver también

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
