---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Sposta il cursore su una cella della tabella nella sezione corrente.
type: docs
weight: 510
url: /it/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Sposta il cursore su una cella della tabella nella sezione corrente.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableIndex | Int32 | Indice della tabella in cui spostarsi. |
| rowIndex | Int32 | L'indice della riga nella tabella. |
| columnIndex | Int32 | L'indice della colonna nella tabella. |
| characterIndex | Int32 | L'indice del carattere all'interno della cella. Un valore negativo consente di specificare una posizione dalla fine della cella. Usa -1 per spostarti alla fine di la cella. |

### Osservazioni

La navigazione viene effettuata all'interno della storia corrente della sezione corrente.

Per i parametri dell'indice, quando indice è maggiore o uguale a 0, specifica un indice da l'inizio con 0 come primo elemento. Quando l'indice è inferiore a 0, viene specificato un indice da alla fine con -1 come ultimo elemento.

### Esempi

Mostra come spostare il cursore di un generatore di documenti su una cella in una tabella.

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
// Possiamo spostare nuovamente il cursore all'interno della tabella su una cella specifica.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


