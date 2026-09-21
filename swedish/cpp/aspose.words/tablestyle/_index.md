---
title: "Aspose::Words::TableStyle-klass"
linktitle: "TableStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TableStyle-klass. Representerar en tabellstil. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 67000
url: /sv/cpp/aspose.words/tablestyle/
---
## TableStyle class


Representerar en tabellstil. För att läsa mer, besök [Arbeta med tabeller](https://docs.aspose.com/words/cpp/working-with-tables/) dokumentationsartikel.

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Jämför med den angivna stilen. Stil-ID:n jämförs endast för inbyggda stilar. Standardvärden för stilar inkluderas inte i jämförelsen. Grundstil, länkad stil och nästa styckestil jämförs rekursivt. |
| [get_Aliases](../style/get_aliases/)() | Hämtar alla alias för denna stil. Om stilen inte har några alias returneras en tom strängarray. |
| [get_Alignment](./get_alignment/)() | Anger justeringen för tabellstilen. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Hämtar eller anger en flagga som indikerar om text i en tabellrad får delas över en sidbrytning. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Anger om denna stil automatiskt omdefinieras baserat på det lämpliga värdet. |
| [get_BaseStyleName](../style/get_basestylename/)() | Hämtar/anger namnet på den stil som denna stil är baserad på. |
| [get_Borders](./get_borders/)() | Hämtar samlingen av standardcellkanter för stilen. |
| [get_BottomPadding](./get_bottompadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under innehållet i tabellceller. |
| [get_BuiltIn](../style/get_builtin/)() | Sant om denna stil är en av de inbyggda stilarna i MS Word. |
| [get_CellSpacing](./get_cellspacing/)() | Hämtar eller anger mängden utrymme (i punkter) mellan cellerna. |
| [get_ColumnStripe](./get_columnstripe/)() | Hämtar eller anger antalet kolumner som ska inkluderas i bandning när stilen specificerar ojämna/jämna kolumnband. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Samling av villkorliga stilar som kan definieras för denna tabellstil. |
| [get_Document](../style/get_document/)() | Hämtar ägardokumentet. |
| [get_Font](../style/get_font/)() | Hämtar teckenformateringen för stilen. |
| [get_IsHeading](../style/get_isheading/)() | Sant när stilen är en av de inbyggda rubrikstilarna. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Anger om denna stil visas i det snabba [Style](../style/)-galleriet i MS Word‑gränssnittet. |
| [get_LeftIndent](./get_leftindent/)() | Hämtar eller anger värdet som representerar vänsterindraget för en tabell. |
| [get_LeftPadding](./get_leftpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till vänster om innehållet i tabellceller. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Hämtar/anger namnet på den [Style](../style/) som är länkad till denna. Returnerar en tom sträng om inga stilar är länkade. |
| [get_List](../style/get_list/)() | Hämtar listan som definierar formateringen för denna liststil. |
| [get_ListFormat](../style/get_listformat/)() | Tillhandahåller åtkomst till listformateringsegenskaperna för en styckestil. |
| [get_Locked](../style/get_locked/)() const | Anger om denna stil är låst. |
| [get_Name](../style/get_name/)() const | Hämtar eller anger namnet på stilen. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Hämtar/anger namnet på stilen som ska tillämpas automatiskt på ett nytt stycke som infogas efter ett stycke formaterat med den angivna stilen. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Hämtar styckeformateringen för stilen. |
| [get_Priority](../style/get_priority/)() const | Hämtar/anger det heltal som representerar prioriteten för sortering av stilar i Stilpanelen. |
| [get_RightPadding](./get_rightpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till höger om innehållet i tabellceller. |
| [get_RowStripe](./get_rowstripe/)() | Hämtar eller anger antalet rader som ska inkluderas i bandning när stilen specificerar ojämna/jämna radband. |
| [get_SemiHidden](../style/get_semihidden/)() const | Hämtar/anger om stilen är dold i Stilgalleriet och i Stilpanelen. |
| [get_Shading](./get_shading/)() | Hämtar ett [Shading](../shading/)-objekt som hänvisar till skuggningsformateringen för tabellceller. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Hämtar den språkoberoende stilidentifieraren för en inbyggd stil. |
| [get_Styles](../style/get_styles/)() const | Hämtar samlingen av stilar som denna stil tillhör. |
| [get_TopPadding](./get_toppadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till ovanför innehållet i tabellceller. |
| [get_Type](../style/get_type/)() const | Hämtar stiltypen (stycke eller tecken). |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Hämtar/anger om stilen som används i det aktuella dokumentet visas igen i Stilgalleriet och i Stilpanelen. Sant när den använda stilen ska visas i Stilgalleriet. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Anger den vertikala justeringen för cellerna. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Tar bort den angivna stilen från dokumentet. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Sättare för [Aspose::Words::TableStyle::get_Alignment](./get_alignment/). |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Sättare för [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | Sättare för [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/). |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | Sättare för [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Sättare för [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Sättare för [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/). |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | Sättare för [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/). |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | Inställning för [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/). |
| [set_LeftIndent](./set_leftindent/)(double) | Inställning för [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Inställning för [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/). |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Inställning för [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Inställning för [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Inställning för [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Inställning för [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Inställning för [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Inställning för [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Inställning för [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Inställning för [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Inställning för [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Inställning för [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Inställning för [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man skapar anpassade stilinställningar för tabellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Att ställa in stilegenskaperna för en tabell kan påverka tabellens egna egenskaper.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Se även

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
