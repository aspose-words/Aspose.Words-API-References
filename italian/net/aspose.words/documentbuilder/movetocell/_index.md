---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words per .NET
description: Esplora senza sforzo il tuo documento con il metodo MoveToCell di DocumentBuilder, posizionando rapidamente il cursore in qualsiasi cella della tabella per una modifica avanzata.
type: docs
weight: 540
url: /it/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Sposta il cursore su una cella della tabella nella sezione corrente.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableIndex | Int32 | Indice della tabella a cui spostarsi. |
| rowIndex | Int32 | L'indice della riga nella tabella. |
| columnIndex | Int32 | L'indice della colonna nella tabella. |
| characterIndex | Int32 | L'indice del carattere all'interno della cella. Un valore negativo consente di specificare una posizione dalla fine della cella. Utilizzare -1 per spostarsi alla fine di cella. |

## Osservazioni

La navigazione avviene all'interno della storia corrente della sezione corrente.

Per i parametri indice, quando indice è maggiore o uguale a 0, specifica un indice da all'inizio, con 0 come primo elemento. Quando indice è minore di 0, specifica un indice da alla fine, con -1 come ultimo elemento.

## Esempi

Mostra come spostare il cursore di un generatore di documenti su una cella di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella 2x2 vuota.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Poiché abbiamo terminato la tabella con il metodo EndTable,
// il cursore del generatore di documenti è attualmente fuori dalla tabella.
// Questo cursore ha la stessa funzione del cursore di testo lampeggiante di Microsoft Word.
// Può anche essere spostato in una posizione diversa nel documento utilizzando i metodi MoveTo del builder.
// Possiamo spostare il cursore all'interno della tabella su una cella specifica.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
