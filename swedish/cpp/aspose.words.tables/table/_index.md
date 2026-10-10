---
title: "Aspose::Words::Tables::Table-klass"
linktitle: "Table"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table-klass. Representerar en tabell i ett Word-dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.tables/table/
---
## Table class


Representerar en tabell i ett Word-dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class Table : public Aspose::Words::CompositeNode
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka slutet av tabellen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare för att besöka början av tabellen. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Ändrar storlek på tabellen och cellerna enligt det angivna auto‑fit‑beteendet. |
| [ClearBorders](./clearborders/)() | Tar bort alla tabell- och cellramar i den här tabellen. |
| [ClearShading](./clearshading/)() | Tar bort all skuggning på tabellen. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Konverterar celler som är horisontellt sammanslagna efter bredd till celler som är sammanslagna med [HorizontalMerge](../cellformat/get_horizontalmerge/). |
| [EnsureMinimum](./ensureminimum/)() | Om tabellen inte har några rader, skapar och lägger till en [Row](../row/). |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Hämtar eller anger absolut horisontell flytande tabellposition som specificeras av tabellens egenskaper, i punkter. Standardvärdet är 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Hämtar eller anger absolut vertikal flytande tabellposition som specificeras av tabellens egenskaper, i punkter. Standardvärdet är 0. |
| [get_Alignment](./get_alignment/)() | Anger hur en inline‑tabell är justerad i dokumentet. |
| [get_AllowAutoFit](./get_allowautofit/)() | Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar innehållet. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | Hämtar eller anger alternativet "Allow spacing between cells". |
| [get_AllowOverlap](./get_allowoverlap/)() | Hämtar om en flytande tabell ska tillåta andra flytande objekt i dokumentet att överlappa dess omfång när den visas. Standardvärdet är **true**. |
| [get_Bidi](./get_bidi/)() | Hämtar eller anger om detta är en höger‑till‑vänster‑tabell. |
| [get_BottomPadding](./get_bottompadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under cellernas innehåll. |
| [get_CellSpacing](./get_cellspacing/)() | Hämtar eller anger mängden utrymme (i punkter) mellan cellerna. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Hämtar antalet omedelbara barn till denna nod. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_Description](./get_description/)() | Hämtar eller anger beskrivning av denna tabell. Den ger en alternativ textrepresentation av informationen som finns i tabellen. |
| [get_DistanceBottom](./get_distancebottom/)() | Hämtar eller anger avståndet mellan tabellens botten och den omgivande texten, i punkter. |
| [get_DistanceLeft](./get_distanceleft/)() | Hämtar eller anger avståndet mellan tabellens vänstra kant och den omgivande texten, i punkter. |
| [get_DistanceRight](./get_distanceright/)() | Hämtar eller anger avståndet mellan tabellens högra kant och den omgivande texten, i punkter. |
| [get_DistanceTop](./get_distancetop/)() | Hämtar eller anger avståndet mellan tabellens topp och den omgivande texten, i punkter. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Hämtar det första barnet till noden. |
| [get_FirstRow](./get_firstrow/)() | Returnerar den första [Row](../row/) noden i tabellen. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returnerar **true** om denna nod har några barnnoder. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Hämtar basobjektet från vilket den horisontella positioneringen av flytande tabell ska beräknas. Standardvärdet är [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returnerar **true** eftersom denna nod kan ha barnnoder. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Hämtar det sista barnet till noden. |
| [get_LastRow](./get_lastrow/)() | Returnerar den sista [Row](../row/) noden i tabellen. |
| [get_LeftIndent](./get_leftindent/)() | Hämtar eller anger värdet som representerar tabellens vänstra indrag. |
| [get_LeftPadding](./get_leftpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till vänster om cellernas innehåll. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [Table](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_PreferredWidth](./get_preferredwidth/)() | Hämtar eller anger tabellens föredragna bredd. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Hämtar eller anger flytande tabells relativa horisontella justering. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Hämtar eller anger flytande tabells relativa vertikala justering. |
| [get_RightPadding](./get_rightpadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till höger om cellernas innehåll. |
| [get_Rows](./get_rows/)() | Tillhandahåller typad åtkomst till tabellens rader. |
| [get_Style](./get_style/)() | Hämtar eller anger tabellstilen som tillämpas på denna tabell. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Hämtar eller anger den lokalt oberoende stilidentifieraren för tabellstilen som tillämpas på denna tabell. |
| [get_StyleName](./get_stylename/)() | Hämtar eller anger namnet på tabellstilen som tillämpas på denna tabell. |
| [get_StyleOptions](./get_styleoptions/)() | Hämtar eller anger bitflaggor som specificerar hur en tabellstil tillämpas på denna tabell. |
| [get_TextWrapping](./get_textwrapping/)() | Hämtar eller anger [TextWrapping](./get_textwrapping/) för tabellen. |
| [get_Title](./get_title/)() | Hämtar eller anger titeln för denna tabell. Den ger en alternativ textrepresentation av informationen som finns i tabellen. |
| [get_TopPadding](./get_toppadding/)() | Hämtar eller anger mängden utrymme (i punkter) som ska läggas ovanför cellernas innehåll. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Hämtar basobjektet från vilket den vertikala positioneringen av flytande tabell ska beräknas. Standardvärdet är [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returnerar en N‑te barnnod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en dynamisk samling av barnnoder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Tillhandahåller stöd för foreach‑stiliteration över barnnoderna i den här noden. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Hämtar texten för den här noden och alla dess barn. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar indexet för den angivna barnnoden i barnnodarrayen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla barnnoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla [SmartTag](../../aspose.words.markup/smarttag/)‑nedärvda noder för den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Väljer en lista med noder som matchar XPath‑uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Väljer den första [Node](../../aspose.words/node/) som matchar XPath‑uttrycket. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | Sättare för [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/). |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | Sättare för [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Sättare för [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/). |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | Sättare för [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/). |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | Sättare för [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/). |
| [set_Bidi](./set_bidi/)(bool) | Sättare för [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Sättare för [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Sättare för [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Sättare för [Aspose::Words::Tables::Table::get_Description](./get_description/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Sättare för [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Sättare för [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Sättare för [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Sättare för [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/). |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Sättare för [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/). |
| [set_LeftIndent](./set_leftindent/)(double) | Sättare för [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Sättare för [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Sättare för [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Sättare för [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/). |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Sättare för [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/). |
| [set_RightPadding](./set_rightpadding/)(double) | Sättare för [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Sättare för [Aspose::Words::Tables::Table::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Sättare för [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Sättare för [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/). |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | Sättare för [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/). |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | Sättare för [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/). |
| [set_Title](./set_title/)(const System::String\&) | Sättare för [Aspose::Words::Tables::Table::get_Title](./get_title/). |
| [set_TopPadding](./set_toppadding/)(double) | Sättare för [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Sättare för [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/). |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Sätter den angivna tabellramen till den angivna linjestilen, bredden och färgen. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Sätter alla tabellramar till den angivna linjestilen, bredden och färgen. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Ställer in skuggning till de angivna värdena på hela tabellen. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initierar en ny instans av klassen [Table](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

En minimal giltig tabell måste ha minst en [Row](../row/).

## Exempel



Visar hur man bygger en formaterad 2x2-tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// När tabellen byggs kommer dokumentbyggaren att tillämpa sina aktuella RowFormat/CellFormat-egenskapsvärden.
// på den aktuella rad/cell som dess markör befinner sig i och på alla nya rader/celler när den skapar dem.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Tidigare tillagda rader och celler påverkas inte retroaktivt av förändringar i byggarens formatering.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


Visar hur man skapar en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabeller innehåller rader, som innehåller celler, som kan ha stycken
// med typiska element som körningar, former och till och med andra tabeller.
// Att anropa metoden "EnsureMinimum" på en tabell kommer att säkerställa att
// tabellen har minst en rad, cell och stycke.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Lägg till text i den första cellen i den första raden i tabellen.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


Visar hur man itererar genom alla tabeller i dokumentet och skriver ut innehållet i varje cell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Vi kan använda metoden "ToArray" på en rad-samling för att klona den till en array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Vi kan använda metoden "ToArray" på en cell-samling för att klona den till en array.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Se även

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
