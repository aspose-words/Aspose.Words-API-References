---
title: Row.IsLastRow
second_title: Referencia de API de Aspose.Words para .NET
description: Row propiedad. Verdadero si esta es la última fila de una tabla falso en caso contrario.
type: docs
weight: 50
url: /es/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Verdadero si esta es la última fila de una tabla; falso en caso contrario.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../row/)
* asamblea [Aspose.Words](../../../)


