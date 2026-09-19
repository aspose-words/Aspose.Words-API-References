---
title: "Classe Aspose::Words::Tables::CellFormat"
linktitle: "CellFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Tables::CellFormat. Rappresenta tutta la formattazione per una cella di tabella. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Rappresenta tutta la formattazione per una cella di tabella. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Ripristina la formattazione predefinita della cella. Non modifica la larghezza della cella. |
| [get_Borders](./get_borders/)() | Ottiene la collezione dei bordi della cella. |
| [get_BottomPadding](./get_bottompadding/)() | Restituisce o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto della cella. |
| [get_FitText](./get_fittext/)() | Se **true**, adatta il testo nella cella, comprimendo ogni paragrafo alla larghezza della cella. |
| [get_HideMark](./get_hidemark/)() | Restituisce la visibilità del segno della cella. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Specifica come la cella è unita orizzontalmente con altre celle nella riga. |
| [get_LeftPadding](./get_leftpadding/)() | Restituisce o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto della cella. |
| [get_Orientation](./get_orientation/)() | Restituisce o imposta l'orientamento del testo in una cella di tabella. |
| [get_PreferredWidth](./get_preferredwidth/)() | Restituisce o imposta la larghezza preferita della cella. |
| [get_RightPadding](./get_rightpadding/)() | Restituisce o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto della cella. |
| [get_Shading](./get_shading/)() | Restituisce un oggetto [Shading](../../aspose.words/shading/) che si riferisce alla formattazione dell'ombreggiatura per la cella. |
| [get_TopPadding](./get_toppadding/)() | Restituisce o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto della cella. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Restituisce o imposta l'allineamento verticale del testo nella cella. |
| [get_VerticalMerge](./get_verticalmerge/)() | Specifica come la cella viene unita ad altre celle verticalmente. |
| [get_Width](./get_width/)() | Ottiene la larghezza della cella in punti. |
| [get_WrapText](./get_wraptext/)() | Se **true**, avvolge il testo per la cella. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Impostatore per [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Impostatore per [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Imposta la visibilità del marcatore della cella. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Impostatore per [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Impostatore per [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Impostatore per [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Impostatore per [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Impostatore per [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Impostatore per [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Impostatore per [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Impostatore per [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Impostatore per [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Impostatore per [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Imposta la quantità di spazio (in punti) da aggiungere a sinistra/sopra/destra/sotto del contenuto della cella. |
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


Mostra come modificare la formattazione di una cella di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Utilizza la proprietà "CellFormat" di una cella per impostare la formattazione che modifica l'aspetto di quella cella.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
