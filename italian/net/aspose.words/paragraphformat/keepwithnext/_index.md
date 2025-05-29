---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words per .NET
description: Scopri come la proprietà KeepWithNext di ParagraphFormat garantisce che i paragrafi restino uniti, migliorando il flusso e la leggibilità del documento, per un aspetto curato.
type: docs
weight: 170
url: /it/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Vero se il paragrafo deve rimanere sulla stessa pagina del paragrafo che lo segue.

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
