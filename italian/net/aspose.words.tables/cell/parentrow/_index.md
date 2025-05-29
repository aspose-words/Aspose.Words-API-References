---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words per .NET
description: Scopri la proprietà Cell ParentRow per accedere facilmente alla riga padre di qualsiasi cella, migliorando l'efficienza della gestione dei dati e della navigazione.
type: docs
weight: 100
url: /it/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

Restituisce la riga padre della cella.

```csharp
public Row ParentRow { get; }
```

## Esempi

Mostra come apparecchiare la tavola in modo che tutti siano sulla stessa lunghezza d'onda.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Abilitazione di KeepWithNext per ogni paragrafo nella tabella eccetto per
// gli ultimi nell'ultima riga impediranno che la tabella venga suddivisa su più pagine.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
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
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
