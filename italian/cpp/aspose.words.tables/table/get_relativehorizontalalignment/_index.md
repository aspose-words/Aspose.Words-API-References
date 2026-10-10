---
title: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment metodo"
linktitle: "get_RelativeHorizontalAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment metodo. Ottiene o imposta l'allineamento orizzontale relativo della tabella flottante in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.tables/table/get_relativehorizontalalignment/
---
## Table::get_RelativeHorizontalAlignment method


Ottiene o imposta l'allineamento orizzontale relativo della tabella fluttuante.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment()
```


## Esempi



Mostra come impostare la posizione delle tabelle fluttuanti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Imposta la posizione della tabella in un punto della pagina, ad esempio, in questo caso, nell'angolo inferiore destro.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Possiamo anche impostare un offset orizzontale e verticale in punti dalla posizione del paragrafo dove abbiamo inserito la tabella.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Vedi anche

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
