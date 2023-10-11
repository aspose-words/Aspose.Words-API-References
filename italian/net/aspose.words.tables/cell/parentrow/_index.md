---
title: Cell.ParentRow
second_title: Aspose.Words per .NET API Reference
description: Cell proprietà. Restituisce la riga madre della cella.
type: docs
weight: 100
url: /it/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Restituisce la riga madre della cella.

```csharp
public Row ParentRow { get; }
```

### Osservazioni

Equivalente aFirstNonMarkupParentNode lanciato a[`Row`](../../row/).

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

* class [Row](../../row/)
* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../cell/)
* assemblea [Aspose.Words](../../../)


