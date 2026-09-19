---
title: "Aspose::Words::Tables::PreferredWidth::FromPoints metodo"
linktitle: "FromPoints"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::PreferredWidth::FromPoints metodo. Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata usando un numero di punti in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth::FromPoints method


Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata usando un numero di punti.

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::PreferredWidth::FromPoints(double points)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore deve essere compreso tra 0 e 22 pollici (22 * 72 punti). |

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


Mostra come utilizzare gli strumenti di conversione delle unità specificando una larghezza preferita per una cella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(Aspose::Words::ConvertUtil::InchToPoint(3)));
builder->InsertCell();

ASPOSE_ASSERT_EQ(216.0, table->get_FirstRow()->get_FirstCell()->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Vedi anche

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
