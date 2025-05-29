---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words para .NET
description: Descubra la propiedad Row IsLastRow. Identifique fácilmente si una fila es la última de una tabla para optimizar la gestión de datos y optimizar la programación.
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

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
