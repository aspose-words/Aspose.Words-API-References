---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words para .NET
description: Descubra la propiedad Cell ParentRow para acceder fácilmente a la fila principal de cualquier celda, mejorando la gestión de datos y la eficiencia de navegación.
type: docs
weight: 100
url: /es/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Devuelve la fila principal de la celda.

```csharp
public Row ParentRow { get; }
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

* class [Row](../../row/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
