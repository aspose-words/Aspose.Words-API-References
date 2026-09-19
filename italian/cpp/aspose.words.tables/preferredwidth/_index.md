---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::PreferredWidth class. Rappresenta un valore e la sua unità di misura utilizzati per specificare la larghezza preferita di una tabella o di una cella. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Rappresenta un valore e la sua unità di misura utilizzati per specificare la larghezza preferita di una tabella o di una cella. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| static [Auto](./auto/)() | Restituisce un'istanza che rappresenta il valore "larghezza preferita non specificata". |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Determina se il [PreferredWidth](./) specificato è uguale in valore al [PreferredWidth](./) corrente. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| static [FromPercent](./frompercent/)(double) | Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata come percentuale. |
| static [FromPoints](./frompoints/)(double) | Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata usando un numero di punti. |
| [get_Type](./get_type/)() const | Ottiene l'unità di misura utilizzata per questo valore di larghezza preferita. |
| [get_Value](./get_value/)() const | Ottiene il valore della larghezza preferita. L'unità di misura è specificata nella proprietà [Type](./get_type/). |
| [GetHashCode](./gethashcode/)() const override | Funziona come funzione hash per questo tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Restituisce una stringa leggibile dall'utente che visualizza il valore di questo oggetto. |
| static [Type](./type/)() |  |
## Note


La larghezza preferita può essere specificata come percentuale, numero di punti o un valore speciale "none/auto".

Le istanze di questa classe sono immutabili.

## Esempi



Mostra come impostare una tabella per adattarsi automaticamente al 50% della larghezza della pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
