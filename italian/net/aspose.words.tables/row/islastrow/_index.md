---
title: Row.IsLastRow
second_title: Aspose.Words per .NET API Reference
description: Row proprietà. Vero se questa è lultima riga in una tabella falso altrimenti.
type: docs
weight: 50
url: /it/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Vero se questa è l'ultima riga in una tabella; falso altrimenti.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../row/)
* assemblea [Aspose.Words](../../../)


