---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words para .NET
description: Row IsLastRow propiedad. Verdadero si esta es la última fila de una tabla falso en caso contrario en C#.
type: docs
weight: 50
url: /es/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Verdadero si esta es la última fila de una tabla; falso en caso contrario.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
