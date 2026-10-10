---
title: "Aspose::Words::DocumentBuilder class"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder class. Tillhandahåller metoder för att infoga text, bilder och annat innehåll, specificera teckensnitt, stycke- och sektionformatering. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words/documentbuilder/
---
## DocumentBuilder class


Tillhandahåller metoder för att infoga text, bilder och annat innehåll, ange teckensnitt, stycke- och sektionsformatering. För att läsa mer, besök artikeln [Document Builder Overview](https://docs.aspose.com/words/cpp/document-builder-overview/) i dokumentationen.

```cpp
class DocumentBuilder : public Aspose::Words::IRunAttrSource,
                        public Aspose::Words::IParaAttrSource,
                        public Aspose::Words::IRowAttrSource,
                        public Aspose::Words::ICellAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [DeleteRow](./deleterow/)(int32_t, int32_t) | Tar bort en rad från en tabell. |
| [DocumentBuilder](./documentbuilder/)() | Initierar en ny instans av den här klassen. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initierar en ny instans av den här klassen. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initierar en ny instans av den här klassen. |
| [DocumentBuilder](./documentbuilder/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) | Initierar en ny instans av den här klassen. |
| [EndBookmark](./endbookmark/)(const System::String\&) | Markerar den aktuella positionen i dokumentet som ett bokmärkes slut. |
| [EndColumnBookmark](./endcolumnbookmark/)(const System::String\&) | Markerar den aktuella positionen i dokumentet som ett kolumnbokmärkes slut. Positionen måste vara i en tabellcell. |
| [EndEditableRange](./endeditablerange/)() | Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut. |
| [EndEditableRange](./endeditablerange/)(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) | Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut. |
| [EndRow](./endrow/)() | Avslutar en tabellrad i dokumentet. |
| [EndTable](./endtable/)() | Avslutar en tabell i dokumentet. |
| [get_Bold](./get_bold/)() | Sant om teckensnittet är formaterat som fetstil. |
| [get_CellFormat](./get_cellformat/)() | Returnerar ett objekt som representerar de aktuella formateringsegenskaperna för tabellcellen. |
| [get_CurrentNode](./get_currentnode/)() | Hämtar noden som för närvarande är markerad i denna [DocumentBuilder](./). |
| [get_CurrentParagraph](./get_currentparagraph/)() | Hämtar stycket som för närvarande är markerat i denna [DocumentBuilder](./). |
| [get_CurrentSection](./get_currentsection/)() | Hämtar sektionen som för närvarande är markerad i denna [DocumentBuilder](./). |
| [get_CurrentStory](./get_currentstory/)() | Hämtar historien som för närvarande är markerad i denna [DocumentBuilder](./). |
| [get_CurrentStructuredDocumentTag](./get_currentstructureddocumenttag/)() | Hämtar den strukturerade dokumenttaggen som för närvarande är markerad i denna [DocumentBuilder](./). |
| [get_Document](./get_document/)() const | Hämtar eller anger [Document](./get_document/)‑objektet som detta objekt är kopplat till. |
| [get_Font](./get_font/)() | Returnerar ett objekt som representerar aktuella teckensnittsegenskaper för formatering. |
| [get_IsAtEndOfParagraph](./get_isatendofparagraph/)() | Returnerar **true** om markören är i slutet av det aktuella stycket. |
| [get_IsAtEndOfStructuredDocumentTag](./get_isatendofstructureddocumenttag/)() | Returnerar **true** om markören är i slutet av en strukturerad dokumenttagg. |
| [get_IsAtStartOfParagraph](./get_isatstartofparagraph/)() | Returnerar **true** om markören är i början av det aktuella stycket (ingen text före markören). |
| [get_Italic](./get_italic/)() | Sant om teckensnittet är formaterat som kursiv. |
| [get_ListFormat](./get_listformat/)() | Returnerar ett objekt som representerar aktuella listformateringsegenskaper. |
| [get_PageSetup](./get_pagesetup/)() | Returnerar ett objekt som representerar aktuella sidinställnings‑ och sektionsegenskaper. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Returnerar ett objekt som representerar aktuella styckeformateringsegenskaper. |
| [get_RowFormat](./get_rowformat/)() | Returnerar ett objekt som representerar aktuella tabellradsformateringsegenskaper. |
| [get_Underline](./get_underline/)() | Hämtar/anger understryknings typ för det aktuella teckensnittet. |
| [GetType](./gettype/)() const override |  |
| [InsertBreak](./insertbreak/)(Aspose::Words::BreakType) | Infogar ett avbrott av angiven typ i dokumentet. |
| [InsertCell](./insertcell/)() | Infogar en tabellcell i dokumentet. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertChart](./insertchart/)(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) | Infogar ett diagramobjekt i dokumentet och skalar det till angiven storlek. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, int32_t) | Infogar ett kryssruteformulärfält på den aktuella positionen. |
| [InsertCheckBox](./insertcheckbox/)(const System::String\&, bool, bool, int32_t) | Infogar ett kryssruteformulärfält på den aktuella positionen. |
| [InsertComboBox](./insertcombobox/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, int32_t) | Infogar ett kombinationsruteformulärfält på den aktuella positionen. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Infogar ett dokument på markörens position. |
| [InsertDocument](./insertdocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Infogar ett dokument på markörens position. |
| [InsertDocumentInline](./insertdocumentinline/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Infogar ett dokument inline på markörens position. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool) | Infogar ett Word‑fält i ett dokument och uppdaterar eventuellt fältresultatet. |
| [InsertField](./insertfield/)(const System::String\&) | Infogar ett Word‑fält i ett dokument och uppdaterar fältresultatet. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&) | Infogar ett Word‑fält i ett dokument utan att uppdatera fältresultatet. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&) | Infogar en fotnot eller slutnot i dokumentet. |
| [InsertFootnote](./insertfootnote/)(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) | Infogar en fotnot eller slutnot i dokumentet. |
| [InsertForms2OleControl](./insertforms2olecontrol/)(const System::SharedPtr\<Aspose::Words::Drawing::Ole::Forms2OleControl\>\&) | Infogar [Forms2OleControl](../)‑objektet på den aktuella positionen. |
| [InsertGroupShape](./insertgroupshape/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Grupperar de former som skickas som parameter till en ny GroupShape‑nod som infogas på den aktuella positionen. |
| [InsertGroupShape](./insertgroupshape/)(double, double, double, double, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\>\&) | Grupperar formerna som skickas som en parameter till en ny GroupShape node av den angivna storleken som infogas på den angivna positionen. |
| [InsertHorizontalRule](./inserthorizontalrule/)() | Infogar en horisontell linjeform i dokumentet. |
| [InsertHtml](./inserthtml/)(const System::String\&) | Infogar en HTML-sträng i dokumentet. |
| [InsertHtml](./inserthtml/)(const System::String\&, bool) | Infogar en HTML-sträng i dokumentet. |
| [InsertHtml](./inserthtml/)(const System::String\&, Aspose::Words::HtmlInsertOptions) | Infogar en HTML-sträng i dokumentet. Tillåter att ange ytterligare alternativ. |
| [InsertHyperlink](./inserthyperlink/)(const System::String\&, const System::String\&, bool) | Infogar en hyperlänk i dokumentet. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Infogar en bild från ett **Image**-objekt i dokumentet. Bilden infogas inline och med 100 % skala. |
| [InsertImage](./insertimage/)(const System::String\&) | Infogar en bild från en fil eller URL i dokumentet. Bilden infogas inline och med 100 % skala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Infogar en bild från en ström i dokumentet. Bilden infogas inline och med 100 % skala. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&) | Infogar en bild från en byte-array i dokumentet. Bilden infogas inline och med 100 % skala. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, double, double) | Infogar en inline-bild från ett **Image**-objekt i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](./insertimage/)(const System::String\&, double, double) | Infogar en inline-bild från en fil eller URL i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, double, double) | Infogar en inline-bild från en ström i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, double, double) | Infogar en inline-bild från en byte-array i dokumentet och skalar den till den angivna storleken. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar en bild från ett **Image**-objekt på den angivna positionen och storleken. |
| [InsertImage](./insertimage/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar en bild från en fil eller URL på den angivna positionen och storleken. |
| [InsertImage](./insertimage/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar en bild från en ström på den angivna positionen och storleken. |
| [InsertImage](./insertimage/)(const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar en bild från en byte-array på den angivna positionen och storleken. |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, double, double) |  |
| [InsertImage](./insertimage/)(std::basic_istream\<CharType, Traits\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) |  |
| [InsertNode](./insertnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod före markören. |
| [InsertOleObject](./insertoleobject/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Infogar ett inbäddat OLE-objekt från en ström i dokumentet. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Detekterar OLE-objekttyp med hjälp av filändelse. |
| [InsertOleObject](./insertoleobject/)(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) | Infogar ett inbäddat eller länkat OLE-objekt från en fil i dokumentet. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter. |
| [InsertOleObject](./insertoleobject/)(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObject](./insertoleobject/)(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) |  |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, bool, const System::String\&, const System::String\&) | Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av filändelse. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) | Infogar ett inbäddat eller länkat OLE-objekt som ikon i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) | Infogar ett inbäddat OLE-objekt som ikon från en ström i dokumentet. Tillåter att ange ikonfil och bildtext. Detekterar OLE-objekttyp med hjälp av angivet progID-parameter. |
| [InsertOleObjectAsIcon](./insertoleobjectasicon/)(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) |  |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, double, double) | Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) | Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertOnlineVideo](./insertonlinevideo/)(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar ett online-videobjekt i dokumentet och skalar det till den angivna storleken. |
| [InsertParagraph](./insertparagraph/)() | Infogar en styckebrytning i dokumentet. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, double, double) | Infogar en inline-form med angiven typ och storlek. |
| [InsertShape](./insertshape/)(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) | Infogar en fristående form med angiven position, storlek och typ av textomslag. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) | Infogar en signaturrad på den aktuella positionen. |
| [InsertSignatureLine](./insertsignatureline/)(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) | Infogar en signaturrad på den angivna positionen. |
| [InsertStructuredDocumentTag](./insertstructureddocumenttag/)(Aspose::Words::Markup::SdtType) | Infogar en [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) i dokumentet. |
| [InsertStyleSeparator](./insertstyleseparator/)() | Infogar stilseparator i dokumentet. |
| [InsertTableOfContents](./inserttableofcontents/)(const System::String\&) | Infogar ett TOC (innehållsförteckning) fält i dokumentet. |
| [InsertTextInput](./inserttextinput/)(const System::String\&, Aspose::Words::Fields::TextFormFieldType, const System::String\&, const System::String\&, int32_t) | Infogar ett textformulärfält på den aktuella positionen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MoveTo](./moveto/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Flyttar markören till en inline-nod eller till slutet av ett stycke. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&) | Flyttar markören till ett bokmärke. |
| [MoveToBookmark](./movetobookmark/)(const System::String\&, bool, bool) | Flyttar markören till ett bokmärke med högre precision. |
| [MoveToCell](./movetocell/)(int32_t, int32_t, int32_t, int32_t) | Flyttar markören till en tabellcell i den aktuella sektionen. |
| [MoveToDocumentEnd](./movetodocumentend/)() | Flyttar markören till slutet av dokumentet. |
| [MoveToDocumentStart](./movetodocumentstart/)() | Flyttar markören till början av dokumentet. |
| [MoveToField](./movetofield/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&, bool) | Flyttar markören till ett fält i dokumentet. |
| [MoveToHeaderFooter](./movetoheaderfooter/)(Aspose::Words::HeaderFooterType) | Flyttar markören till början av ett sidhuvud eller sidfot i den aktuella sektionen. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&) | Flyttar markören till en position strax bortom det angivna sammanslagningsfältet och tar bort sammanslagningsfältet. |
| [MoveToMergeField](./movetomergefield/)(const System::String\&, bool, bool) | Flyttar sammanslagningsfältet till det angivna sammanslagningsfältet. |
| [MoveToParagraph](./movetoparagraph/)(int32_t, int32_t) | Flyttar markören till ett stycke i den aktuella sektionen. |
| [MoveToSection](./movetosection/)(int32_t) | Flyttar markören till början av kroppen i en angiven sektion. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(int32_t, int32_t) | Flyttar markören till en strukturerad dokumenttagg i den aktuella sektionen. |
| [MoveToStructuredDocumentTag](./movetostructureddocumenttag/)(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) | Flyttar markören till den strukturerade dokumenttaggen. |
| [PopFont](./popfont/)() | Hämtar teckenformatering som tidigare sparats på stacken. |
| [PushFont](./pushfont/)() | Sparar aktuell teckenformatering på stacken. |
| [set_Bold](./set_bold/)(bool) | Inställare för [Aspose::Words::DocumentBuilder::get_Bold](./get_bold/). |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Inställare för [Aspose::Words::DocumentBuilder::get_Document](./get_document/). |
| [set_Italic](./set_italic/)(bool) | Inställare för [Aspose::Words::DocumentBuilder::get_Italic](./get_italic/). |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | Inställare för [Aspose::Words::DocumentBuilder::get_Underline](./get_underline/). |
| [StartBookmark](./startbookmark/)(const System::String\&) | Markerar den aktuella positionen i dokumentet som en bokmärkestart. |
| [StartColumnBookmark](./startcolumnbookmark/)(const System::String\&) | Markerar den aktuella positionen i dokumentet som en kolumnbokmärkestart. Positionen måste vara i en tabellcell. |
| [StartEditableRange](./starteditablerange/)() | Markerar den aktuella positionen i dokumentet som en redigerbar områdesstart. |
| [StartTable](./starttable/)() | Startar en tabell i dokumentet. |
| static [Type](./type/)() |  |
| [Write](./write/)(const System::String\&) | Infogar en sträng i dokumentet på den aktuella infogningspositionen. |
| [Writeln](./writeln/)(const System::String\&) | Infogar en sträng och ett styckebrott i dokumentet. |
| [Writeln](./writeln/)() | Infogar en styckebrytning i dokumentet. |
## Anmärkningar


[DocumentBuilder](./) makes the process of building a [Document](../document/) easier. [Document](../document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](./) is a "facade" for the complex structure of [Document](../document/) and allows to insert content and formatting quickly and easily.

Skapa en [DocumentBuilder](./) och associera den med ett [Document](../document/).

Den [DocumentBuilder](./) har en intern markör där texten kommer att infogas när du anropar [Write()](../), [Writeln()](../), [InsertBreak()](./insertbreak/) och andra metoder. Du kan navigera [DocumentBuilder](./)-markören till en annan plats i ett dokument med hjälp av olika MoveToXXX‑metoder.

Använd egenskapen [Font](./get_font/) för att ange teckenformatering som kommer att tillämpas på all text som infogas från den aktuella positionen i dokumentet och framåt.

Använd egenskapen [ParagraphFormat](./get_paragraphformat/) för att ange styckeformatering för det aktuella och alla stycken som kommer att infogas.

Använd egenskapen [PageSetup](./get_pagesetup/) för att ange sid- och sektionsinställningar för den aktuella sektionen och alla sektioner som kommer att infogas.

Använd egenskaperna [CellFormat](./get_cellformat/) och [RowFormat](./get_rowformat/) för att ange formateringsinställningar för tabellceller och rader. Använd metoderna [InsertCell](./insertcell/) och [EndRow](./endrow/) för att bygga en tabell.

Observera att egenskaperna [Font](./get_font/), [ParagraphFormat](./get_paragraphformat/) och [PageSetup](./get_pagesetup/) uppdateras varje gång du navigerar till en annan plats i dokumentet för att återspegla de formateringsinställningar som är tillgängliga på den nya platsen.

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


Visar hur man använder en dokumentbyggare för att skapa en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Starta tabellen, fyll sedan den första raden med två celler.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Anropa builderns "EndRow"-metod för att starta en ny rad.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
