---
title: "Aspose::Words::Tables::Table::ClearShading metodo"
linktitle: "ClearShading"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::ClearShading metodo. Rimuove tutte le sfumature sulla tabella in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.tables/table/clearshading/
---
## Table::ClearShading method


Rimuove tutte le sfumature nella tabella.

```cpp
void Aspose::Words::Tables::Table::ClearShading()
```


## Esempi



Mostra come applicare un bordo di contorno a una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Allinea la tabella al centro della pagina.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Rimuovi eventuali bordi e ombreggiature esistenti dalla tabella.
table->ClearBorders();
table->ClearShading();

// Aggiungi bordi verdi al contorno della tabella.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Riempi le celle con un colore verde chiaro solido.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
