---
title: "Metodo Aspose::Words::DocumentBuilder::MoveToCell"
linktitle: "MoveToCell"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::MoveToCell. Sposta il cursore su una cella di tabella nella sezione corrente in C++."
type: docs
weight: 53000
url: /it/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Sposta il cursore su una cella di tabella nella sezione corrente.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableIndex | int32_t | L'indice della tabella a cui spostarsi. |
| rowIndex | int32_t | L'indice della riga nella tabella. |
| columnIndex | int32_t | L'indice della colonna nella tabella. |
| characterIndex | int32_t | L'indice del carattere all'interno della cella. Un valore negativo consente di specificare una posizione dalla fine della cella. Usa -1 per spostarti alla fine della cella. |
## Note


La navigazione viene eseguita all'interno della storia corrente della sezione corrente.

Per i parametri indice, quando l'indice è maggiore o uguale a 0, specifica un indice dall'inizio, con 0 che rappresenta il primo elemento. Quando l'indice è minore di 0, specifica un indice dalla fine, con -1 che rappresenta l'ultimo elemento.

## Esempi



Mostra come spostare il cursore di un document builder su una cella di una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una tabella vuota 2x2.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Poiché abbiamo terminato la tabella con il metodo EndTable,
// il cursore del document builder è attualmente fuori dalla tabella.
// Questo cursore ha la stessa funzione del cursore lampeggiante di Microsoft Word.
// Può anche essere spostato in una posizione diversa nel documento usando i metodi MoveTo del builder.
// Possiamo spostare nuovamente il cursore all'interno della tabella su una cella specifica.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
