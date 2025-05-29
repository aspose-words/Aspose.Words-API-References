---
title: Row.IsLastRow
linktitle: IsLastRow
articleTitle: IsLastRow
second_title: Aspose.Words per .NET
description: Scopri la proprietà Row IsLastRow. Identifica facilmente se una riga è l'ultima di una tabella, semplificando la gestione dei dati e migliorando l'efficienza di programmazione.
type: docs
weight: 50
url: /it/net/aspose.words.tables/row/islastrow/
---
## Row.IsLastRow property

Vero se questa è l'ultima riga di una tabella; falso in caso contrario.

```csharp
public bool IsLastRow { get; }
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

* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
