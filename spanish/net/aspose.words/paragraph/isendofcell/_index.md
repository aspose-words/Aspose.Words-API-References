---
title: IsEndOfCell
second_title: Referencia de API de Aspose.Words para .NET
description: Verdadero si este párrafo es el último párrafo de unCellaspose.words.tables/cell  falso en caso contrario.
type: docs
weight: 50
url: /es/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Verdadero si este párrafo es el último párrafo de un[`Cell`](../../../aspose.words.tables/cell) ; falso en caso contrario.

```csharp
public bool IsEndOfCell { get; }
```

### Ejemplos

Muestra cómo configurar una mesa para permanecer juntos en la misma página.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Habilitar KeepWithNext para cada párrafo de la tabla excepto para el
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

* class [Paragraph](../../paragraph)
* espacio de nombres [Aspose.Words](../../paragraph)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
