---
title: "Aspose::Words::Tables::Table classe"
linktitle: "Table"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table classe. Rappresenta una tabella in un documento Word. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.tables/table/
---
## Table class


Rappresenta una tabella in un documento Word. Per saperne di più, visita l'articolo di documentazione [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class Table : public Aspose::Words::CompositeNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine della tabella. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio della tabella. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato. |
| [ClearBorders](./clearborders/)() | Rimuove tutti i bordi della tabella e delle celle in questa tabella. |
| [ClearShading](./clearshading/)() | Rimuove tutte le sfumature nella tabella. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Converte le celle fuse orizzontalmente per larghezza in celle fuse tramite [HorizontalMerge](../cellformat/get_horizontalmerge/). |
| [EnsureMinimum](./ensureminimum/)() | Se la tabella non ha righe, crea e aggiunge una [Row](../row/). |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Ottiene o imposta la posizione orizzontale assoluta della tabella fluttuante specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Ottiene o imposta la posizione verticale assoluta della tabella fluttuante specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [get_Alignment](./get_alignment/)() | Specifica come una tabella in linea è allineata nel documento. |
| [get_AllowAutoFit](./get_allowautofit/)() | Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle in una tabella per adattarle al loro contenuto. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | Ottiene o imposta l'opzione "Allow spacing between cells". |
| [get_AllowOverlap](./get_allowoverlap/)() | Ottiene se una tabella fluttuante deve consentire ad altri oggetti fluttuanti nel documento di sovrapporsi alle sue dimensioni quando visualizzata. Il valore predefinito è **true**. |
| [get_Bidi](./get_bidi/)() | Ottiene o imposta se questa è una tabella da destra a sinistra. |
| [get_BottomPadding](./get_bottompadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle. |
| [get_CellSpacing](./get_cellspacing/)() | Ottiene o imposta la quantità di spazio (in punti) tra le celle. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_Description](./get_description/)() | Ottiene o imposta la descrizione di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [get_DistanceBottom](./get_distancebottom/)() | Ottiene o imposta la distanza tra il fondo della tabella e il testo circostante, in punti. |
| [get_DistanceLeft](./get_distanceleft/)() | Ottiene o imposta la distanza tra il lato sinistro della tabella e il testo circostante, in punti. |
| [get_DistanceRight](./get_distanceright/)() | Ottiene o imposta la distanza tra il lato destro della tabella e il testo circostante, in punti. |
| [get_DistanceTop](./get_distancetop/)() | Ottiene o imposta la distanza tra la parte superiore della tabella e il testo circostante, in punti. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FirstRow](./get_firstrow/)() | Restituisce il primo nodo [Row](../row/) nella tabella. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Ottiene l'oggetto base da cui dovrebbe essere calcolata la posizione orizzontale della tabella fluttuante. Il valore predefinito è [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_LastRow](./get_lastrow/)() | Restituisce l'ultimo nodo [Row](../row/) nella tabella. |
| [get_LeftIndent](./get_leftindent/)() | Ottiene o imposta il valore che rappresenta l'indentazione sinistra della tabella. |
| [get_LeftPadding](./get_leftpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [Table](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreferredWidth](./get_preferredwidth/)() | Ottiene o imposta la larghezza preferita della tabella. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Ottiene o imposta l'allineamento orizzontale relativo della tabella fluttuante. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Ottiene o imposta l'allineamento verticale relativo della tabella fluttuante. |
| [get_RightPadding](./get_rightpadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle. |
| [get_Rows](./get_rows/)() | Fornisce un accesso tipizzato alle righe della tabella. |
| [get_Style](./get_style/)() | Ottiene o imposta lo stile della tabella applicato a questa tabella. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile della tabella applicato a questa tabella. |
| [get_StyleName](./get_stylename/)() | Ottiene o imposta il nome dello stile della tabella applicato a questa tabella. |
| [get_StyleOptions](./get_styleoptions/)() | Ottiene o imposta i flag bit che specificano come uno stile di tabella viene applicato a questa tabella. |
| [get_TextWrapping](./get_textwrapping/)() | Ottiene o imposta [TextWrapping](./get_textwrapping/) per la tabella. |
| [get_Title](./get_title/)() | Ottiene o imposta il titolo di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [get_TopPadding](./get_toppadding/)() | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Ottiene l'oggetto base da cui dovrebbe essere calcolata la posizione verticale della tabella fluttuante. Il valore predefinito è [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | Setter per [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/). |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | Setter per [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Setter per [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/). |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | Setter per [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/). |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | Setter per [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/). |
| [set_Bidi](./set_bidi/)(bool) | Setter per [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter per [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Setter per [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Setter per [Aspose::Words::Tables::Table::get_Description](./get_description/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/). |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Impostatore per [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/). |
| [set_LeftIndent](./set_leftindent/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Impostatore per [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Impostatore per [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/). |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Impostatore per [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/). |
| [set_RightPadding](./set_rightpadding/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Impostatore per [Aspose::Words::Tables::Table::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Impostatore per [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Impostatore per [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/). |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | Impostatore per [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/). |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | Impostatore per [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/). |
| [set_Title](./set_title/)(const System::String\&) | Impostatore per [Aspose::Words::Tables::Table::get_Title](./get_title/). |
| [set_TopPadding](./set_toppadding/)(double) | Impostatore per [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Impostatore per [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/). |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Imposta il bordo della tabella specificato allo stile di linea, larghezza e colore specificati. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Imposta tutti i bordi della tabella allo stile di linea, larghezza e colore specificati. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Imposta l'ombreggiatura ai valori specificati sull'intera tabella. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inizializza una nuova istanza della classe [Table](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

Una tabella valida minima deve contenere almeno una [Row](../row/).

## Esempi



Mostra come creare una tabella formattata 2x2.
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

// Durante la creazione della tabella, il costruttore di documenti applicherà i valori delle proprietà RowFormat/CellFormat correnti
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che le crea.
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

// Le righe e le celle aggiunte in precedenza non sono retroattivamente influenzate dalle modifiche al formato del costruttore.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


Mostra come creare una tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Le tabelle contengono righe, che contengono celle, che possono avere paragrafi
// con elementi tipici come run, forme e persino altre tabelle.
// Chiamare il metodo "EnsureMinimum" su una tabella garantirà che
// la tabella abbia almeno una riga, una cella e un paragrafo.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Aggiungi testo alla prima cella nella prima riga della tabella.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


Mostra come iterare attraverso tutte le tabelle nel documento e stampare il contenuto di ogni cella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Possiamo usare il metodo "ToArray" su una raccolta di righe per clonarla in un array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Possiamo usare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
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

## Vedi anche

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
