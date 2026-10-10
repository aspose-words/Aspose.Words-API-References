---
title: "Metodo Aspose::Words::Tables::CellFormat::get_Borders"
linktitle: "get_Borders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::CellFormat::get_Borders. Ottiene la collezione dei bordi della cella in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.tables/cellformat/get_borders/
---
## CellFormat::get_Borders method


Ottiene la collezione dei bordi della cella.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::CellFormat::get_Borders()
```


## Esempi



Mostra come combinare le righe di due tabelle in una sola.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 -  Dalla collezione "Tables" di un nodo Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Utilizzando il metodo "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Aggiungi tutte le righe dalla tabella corrente a quella successiva.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Rimuovi il contenitore della tabella vuota.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Vedi anche

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
