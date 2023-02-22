---
title: ParagraphFormat.KeepWithNext
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Verdadero si el párrafo debe permanecer en la misma página que el párrafo que le sigue.
type: docs
weight: 160
url: /es/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Verdadero si el párrafo debe permanecer en la misma página que el párrafo que le sigue.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


