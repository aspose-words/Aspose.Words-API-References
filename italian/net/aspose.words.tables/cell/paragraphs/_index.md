---
title: Cell.Paragraphs
second_title: Aspose.Words per .NET API Reference
description: Cell proprietà. Ottiene una raccolta di paragrafi che sono figli immediati della cella.
type: docs
weight: 80
url: /it/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

Ottiene una raccolta di paragrafi che sono figli immediati della cella.

```csharp
public ParagraphCollection Paragraphs { get; }
```

### Esempi

Mostra come impostare un tavolo per stare insieme sulla stessa pagina.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Abilitazione KeepWithNext per ogni paragrafo della tabella ad eccezione di
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../cell/)
* assemblea [Aspose.Words](../../../)


