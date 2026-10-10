---
title: "Metodo Aspose::Words::DocumentBuilder::DeleteRow"
linktitle: "DeleteRow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::DeleteRow. Elimina una riga da una tabella in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Elimina una riga da una tabella.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableIndex | int32_t | L'indice della tabella. |
| rowIndex | int32_t | L'indice della riga nella tabella. |

### ReturnValue

Il nodo della riga appena rimosso.
## Note


Se il cursore si trova all'interno della riga che viene eliminata, il cursore viene spostato alla riga successiva o al paragrafo successivo dopo la tabella.

Se elimini una riga da una tabella che contiene solo una riga, l'intera tabella viene eliminata.

Per i parametri indice, quando l'indice è maggiore o uguale a 0, specifica un indice dall'inizio, con 0 che rappresenta il primo elemento. Quando l'indice è minore di 0, specifica un indice dalla fine, con -1 che rappresenta l'ultimo elemento.

## Esempi



Mostra come eliminare una riga da una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Elimina la prima riga della prima tabella nel documento.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Vedi anche

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
