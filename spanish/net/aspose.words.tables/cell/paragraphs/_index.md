---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words para .NET
description: Descubra la propiedad Párrafos de celda para acceder a una colección de párrafos secundarios directos, mejorando la estructura y la legibilidad de su documento.
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
