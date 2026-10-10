---
title: "Aspose::Words::Tables::Table::get_RightPadding metodo"
linktitle: "get_RightPadding"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_RightPadding metodo. Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words.tables/table/get_rightpadding/
---
## Table::get_RightPadding method


Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle.

```cpp
double Aspose::Words::Tables::Table::get_RightPadding()
```


## Esempi



Mostra come configurare il padding del contenuto in una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Per ogni cella nella tabella, impostare la distanza tra il suo contenuto e ciascuno dei suoi bordi.
// Questa tabella manterrà la distanza minima di padding avvolgendo il testo.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
