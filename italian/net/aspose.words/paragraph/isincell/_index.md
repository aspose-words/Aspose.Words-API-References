---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: Aspose.Words per .NET
description: Scopri la proprietà Paragraph IsInCell. Determina facilmente se un paragrafo è figlio diretto di una cella, migliorando la struttura e la formattazione del documento.
type: docs
weight: 100
url: /it/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

Vero se questo paragrafo è un figlio immediato di[`Cell`](../../../aspose.words.tables/cell/) ; falso altrimenti.

```csharp
public bool IsInCell { get; }
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

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
