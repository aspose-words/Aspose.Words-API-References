---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth metodo"
linktitle: "get_PreferredWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth metodo. Restituisce o imposta la larghezza preferita della cella in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Restituisce o imposta la larghezza preferita della cella.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Note


La larghezza preferita (insieme all'opzione Auto Fit della tabella) determina come la larghezza effettiva della cella viene calcolata dall'algoritmo di layout della tabella. Il layout della [Table](../../table/) può essere eseguito da Aspose.Words quando salva il documento o da Microsoft Word quando visualizza il documento.

La larghezza preferita può essere specificata in punti o in percentuale. La larghezza preferita può anche essere specificata come "auto", il che significa che non è specificata alcuna larghezza preferita.

Il valore predefinito è [Auto](../../preferredwidth/auto/).

## Esempi



Mostra come impostare una larghezza preferita per le celle della tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Esistono due modi per applicare la classe "PreferredWidth" alle celle della tabella.
// 1 -  Imposta una larghezza preferita assoluta basata sui punti:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Imposta una larghezza preferita relativa basata sulla percentuale della larghezza della tabella:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Una cella senza larghezza preferita specificata occuperà il resto dello spazio disponibile.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Ogni configurazione della proprietà "PreferredWidth" crea un nuovo oggetto.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Vedi anche

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
