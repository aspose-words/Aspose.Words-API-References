---
title: Cell.ParentRow
second_title: Referencia de API de Aspose.Words para .NET
description: Cell propiedad. Devuelve la fila principal de la celda.
type: docs
weight: 90
url: /es/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Devuelve la fila principal de la celda.

```csharp
public Row ParentRow { get; }
```

### Observaciones

Equivalente a`(Fila) First Non Markup Parent Node`.

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

* class [Row](../../row/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../cell/)
* asamblea [Aspose.Words](../../../)


