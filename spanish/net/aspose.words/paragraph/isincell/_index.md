---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words para .NET
description: Descubra la propiedad "Párrafo IsInCell". Determine fácilmente si un párrafo es un elemento secundario directo de una celda, mejorando así la estructura y el formato de su documento.
type: docs
weight: 100
url: /es/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Verdadero si este párrafo es un hijo inmediato de[`Cell`](../../../aspose.words.tables/cell/) ; falso en caso contrario.

```csharp
public bool IsInCell { get; }
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
