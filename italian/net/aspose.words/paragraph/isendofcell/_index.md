---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsEndOfCell per i paragrafi. Scopri come identificare se un paragrafo è l'ultimo di una cella, migliorando la struttura del tuo documento.
type: docs
weight: 50
url: /it/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

Vero se questo paragrafo è l'ultimo paragrafo di un[`Cell`](../../../aspose.words.tables/cell/) ; falso altrimenti.

```csharp
public bool IsEndOfCell { get; }
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
