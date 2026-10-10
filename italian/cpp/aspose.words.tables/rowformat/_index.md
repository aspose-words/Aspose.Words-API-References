---
title: "Aspose::Words::Tables::RowFormat class"
linktitle: "RowFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::RowFormat class. Rappresenta tutta la formattazione per una riga di tabella. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Rappresenta tutta la formattazione per una riga di tabella. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Ripristina la formattazione predefinita della riga. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Vero se il testo in una riga di tabella è consentito di dividersi attraverso un'interruzione di pagina. |
| [get_Borders](./get_borders/)() | Ottiene la raccolta dei bordi predefiniti delle celle per la riga. |
| [get_HeadingFormat](./get_headingformat/)() | Vero se la riga viene ripetuta come intestazione della tabella su ogni pagina quando la tabella si estende su più di una pagina. |
| [get_Height](./get_height/)() | Ottiene o imposta l'altezza della riga di tabella in punti. |
| [get_HeightRule](./get_heightrule/)() | Ottiene o imposta la regola per determinare l'altezza della riga di tabella. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Impostatore per [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Impostatore per [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | Metodo setter per [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | Metodo setter per [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come costruire una tabella con bordi personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Impostazione delle opzioni di formattazione della tabella per un DocumentBuilder
// le applicherà a ogni riga e cella che aggiungiamo con esso.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Modificando la formattazione la applicherà alla cella corrente,
// e a tutte le nuove celle che creiamo con il builder in seguito.
// Questo non influenzerà le celle che abbiamo aggiunto in precedenza.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta l'altezza della riga per adattare il testo verticale.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Mostra come modificare il formato di righe e celle in una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Usa la proprietà "RowFormat" della prima riga per modificare la formattazione
// del contenuto di tutte le celle in questa riga.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Usa la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Mostra come modificare la formattazione di una riga di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Usa la proprietà "RowFormat" della prima riga per impostare la formattazione che modifica l'aspetto dell'intera riga.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
