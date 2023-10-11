---
title: Paragraph.IsInCell
second_title: Aspose.Words per .NET API Reference
description: Paragraph proprietà. Vero se questo paragrafo è un figlio immediato diCell  falso altrimenti.
type: docs
weight: 100
url: /it/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Vero se questo paragrafo è un figlio immediato di[`Cell`](../../../aspose.words.tables/cell/) ; falso altrimenti.

```csharp
public bool IsInCell { get; }
```

### Esempi

Mostra come apparecchiare una tavola per stare insieme sulla stessa pagina.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Abilita KeepWithNext per ogni paragrafo nella tabella ad eccezione di
// gli ultimi nell'ultima riga impediranno alla tabella di dividersi su più pagine.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)


