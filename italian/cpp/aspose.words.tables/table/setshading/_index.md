---
title: "Metodo Aspose::Words::Tables::Table::SetShading"
linktitle: "SetShading"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Table::SetShading. Imposta l'ombreggiatura ai valori specificati sull'intera tabella in C++."
type: docs
weight: 70000
url: /it/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


Imposta l'ombreggiatura ai valori specificati sull'intera tabella.

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| texture | Aspose::Words::TextureIndex | La texture da applicare. |
| foregroundColor | System::Drawing::Color | Il colore della texture. |
| backgroundColor | System::Drawing::Color | Il colore del riempimento di sfondo. |

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

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
