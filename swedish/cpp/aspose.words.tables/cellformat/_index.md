---
title: "Aspose::Words::Tables::CellFormat klass"
linktitle: "CellFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::CellFormat klass. Representerar all formatering för en tabellcell. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Representerar all formatering för en tabellcell. För att lära dig mer, besök dokumentationsartikeln [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Återställer till standardformatering för cellen. Ändrar inte cellens bredd. |
| [get_Borders](./get_borders/)() | Hämtar samling av cellens kanter. |
| [get_BottomPadding](./get_bottompadding/)() | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till under cellens innehåll. |
| [get_FitText](./get_fittext/)() | Om **true**, anpassar texten i cellen genom att komprimera varje stycke till cellens bredd. |
| [get_HideMark](./get_hidemark/)() | Returnerar synlighet för cellmarkeringen. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Anger hur cellen slås samman horisontellt med andra celler i raden. |
| [get_LeftPadding](./get_leftpadding/)() | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till till vänster om cellens innehåll. |
| [get_Orientation](./get_orientation/)() | Returnerar eller anger orienteringen av text i en tabellcell. |
| [get_PreferredWidth](./get_preferredwidth/)() | Returnerar eller anger den föredragna bredden för cellen. |
| [get_RightPadding](./get_rightpadding/)() | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till till höger om cellens innehåll. |
| [get_Shading](./get_shading/)() | Returnerar ett [Shading](../../aspose.words/shading/)‑objekt som hänvisar till skuggningsformateringen för cellen. |
| [get_TopPadding](./get_toppadding/)() | Returnerar eller anger mängden utrymme (i punkter) som ska läggas till ovanför cellens innehåll. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Returnerar eller anger den vertikala justeringen av text i cellen. |
| [get_VerticalMerge](./get_verticalmerge/)() | Anger hur cellen slås samman med andra celler vertikalt. |
| [get_Width](./get_width/)() | Hämtar cellens bredd i punkter. |
| [get_WrapText](./get_wraptext/)() | Om **true**, radbryt text för cellen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Sättare för [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Sättare för [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Anger synlighet för cellmarkeringen. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Sättare för [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Sättare för [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Sättare för [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Sättare för [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Sättare för [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Sättare för [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Sättare för [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Sättare för [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Sättare för [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Sättare för [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Anger mängden utrymme (i punkter) som ska läggas till vänster/upp/höger/nederst av cellens innehåll. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man bygger en tabell med anpassade kanter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Ställer in tabellformateringsalternativ för en dokumentbyggare
// kommer att tillämpa dem på varje rad och cell som vi lägger till med den.
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

// Att ändra formateringen kommer att tillämpa den på den aktuella cellen,
// och alla nya celler som vi skapar med byggaren efteråt.
// Detta kommer inte att påverka de celler som vi har lagt till tidigare.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Öka radhöjden för att passa den vertikala texten.
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


Visar hur man ändrar formatet för rader och celler i en tabell.
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

// Använd den första radens "RowFormat"-egenskap för att ändra formateringen
// för innehållet i alla celler i denna rad.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Använd "CellFormat"-egenskapen för den första cellen i den sista raden för att ändra formateringen av den cellens innehåll.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Visar hur man ändrar formatering av en tabellcell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Använd en cells egenskap "CellFormat" för att ange formatering som ändrar utseendet på den cellen.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## Se även

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
