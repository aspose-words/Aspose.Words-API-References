---
title: Row
linktitle: Row
articleTitle: Row
second_title: Aspose.Words per .NET
description: Crea facilmente istanze dinamiche di Row con il nostro costruttore Row. Semplifica la gestione dei dati e migliora l'efficienza della tua programmazione oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.tables/row/row/
---
## Row constructor

Inizializza una nuova istanza di[`Row`](../) classe.

```csharp
public Row(DocumentBase doc)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |

## Osservazioni

Quando[`Row`](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e[`ParentNode`](../../../aspose.words/node/parentnode/) È`null`.

Per aggiungere[`Row`](../) all'uso del documento[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) O[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) nella tabella in cui si desidera inserire la riga.

## Esempi

Mostra come creare una tabella nidificata senza utilizzare un generatore di documenti.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Crea la tabella esterna con tre righe e quattro colonne, quindi aggiungila al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crea un'altra tabella con due righe e due colonne e inseriscila nella prima cella della prima tabella.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nuova tabella nel documento con le dimensioni specificate e il testo in ogni cella.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Puoi utilizzare le proprietà "Titolo" e "Descrizione" per aggiungere rispettivamente un titolo e una descrizione alla tua tabella.
    // La tabella deve avere almeno una riga prima di poter utilizzare queste proprietà.
    // Queste proprietà sono significative per i documenti .docx conformi allo standard ISO/IEC 29500 (vedere la classe OoxmlCompliance).
    // Se salviamo il documento in formati precedenti a ISO/IEC 29500, Microsoft Word ignora queste proprietà.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Guarda anche

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
