---
title: "Aspose::Words::Tables::Table Klasse"
linktitle: "Table"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table Klasse. Stellt eine Tabelle in einem Word‑Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.tables/table/
---
## Table class


Stellt eine Tabelle in einem Word-Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class Table : public Aspose::Words::CompositeNode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um das Ende der Tabelle zu besuchen. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher, um den Beginn der Tabelle zu besuchen. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Ändert die Größe von Tabelle und Zellen gemäß dem angegebenen Auto‑Fit‑Verhalten. |
| [ClearBorders](./clearborders/)() | Entfernt alle Tabellen- und Zellenränder in dieser Tabelle. |
| [ClearShading](./clearshading/)() | Entfernt alle Schattierungen in der Tabelle. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Konvertiert horizontal nach Breite zusammengeführte Zellen in Zellen, die durch [HorizontalMerge](../cellformat/get_horizontalmerge/) zusammengeführt sind. |
| [EnsureMinimum](./ensureminimum/)() | Wenn die Tabelle keine Zeilen hat, wird eine [Row](../row/) erstellt und angehängt. |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Liest oder setzt die absolute horizontale Position der schwebenden Tabelle, angegeben durch die Tabelleneigenschaften, in Punkten. Der Standardwert ist 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Liest oder setzt die absolute vertikale Position der schwebenden Tabelle, angegeben durch die Tabelleneigenschaften, in Punkten. Der Standardwert ist 0. |
| [get_Alignment](./get_alignment/)() | Gibt an, wie eine Inline‑Tabelle im Dokument ausgerichtet wird. |
| [get_AllowAutoFit](./get_allowautofit/)() | Ermöglicht Microsoft Word und Aspose.Words, Zellen in einer Tabelle automatisch an deren Inhalt anzupassen. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | Liest oder setzt die Option "Allow spacing between cells". |
| [get_AllowOverlap](./get_allowoverlap/)() | Liest, ob eine schwebende Tabelle anderen schwebenden Objekten im Dokument erlaubt, ihre Ausmaße bei der Anzeige zu überlappen. Der Standardwert ist **true**. |
| [get_Bidi](./get_bidi/)() | Liest oder setzt, ob dies eine rechts‑nach‑links‑Tabelle ist. |
| [get_BottomPadding](./get_bottompadding/)() | Liest oder legt die Menge an Abstand (in Punkten) fest, die unter dem Inhalt von Zellen hinzugefügt wird. |
| [get_CellSpacing](./get_cellspacing/)() | Ruft ab oder legt den Abstand (in Punkten) zwischen den Zellen fest. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ermittelt die Anzahl der direkten Kindknoten dieses Knotens. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_Description](./get_description/)() | Liest oder legt die Beschreibung dieser Tabelle fest. Sie liefert eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [get_DistanceBottom](./get_distancebottom/)() | Liest oder legt den Abstand zwischen dem unteren Rand der Tabelle und dem umgebenden Text in Punkten fest. |
| [get_DistanceLeft](./get_distanceleft/)() | Liest oder legt den Abstand zwischen der linken Seite der Tabelle und dem umgebenden Text in Punkten fest. |
| [get_DistanceRight](./get_distanceright/)() | Liest oder legt den Abstand zwischen der rechten Seite der Tabelle und dem umgebenden Text in Punkten fest. |
| [get_DistanceTop](./get_distancetop/)() | Liest oder legt den Abstand zwischen dem oberen Rand der Tabelle und dem umgebenden Text in Punkten fest. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ermittelt das erste Kind des Knotens. |
| [get_FirstRow](./get_firstrow/)() | Gibt den ersten [Row](../row/) Knoten in der Tabelle zurück. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Gibt **true** zurück, wenn dieser Knoten Kindknoten hat. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Liest das Basisobjekt, von dem die horizontale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert ist [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Gibt **true** zurück, da dieser Knoten Kindknoten haben kann. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ermittelt das letzte Kind des Knotens. |
| [get_LastRow](./get_lastrow/)() | Gibt den letzten [Row](../row/) Knoten in der Tabelle zurück. |
| [get_LeftIndent](./get_leftindent/)() | Liest oder legt den Wert fest, der den linken Einzug der Tabelle darstellt. |
| [get_LeftPadding](./get_leftpadding/)() | Liest oder legt die Menge an Abstand (in Punkten) fest, die links vom Inhalt von Zellen hinzugefügt wird. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt [Table](../../aspose.words/nodetype/) zurück. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_PreferredWidth](./get_preferredwidth/)() | Liest oder legt die bevorzugte Breite der Tabelle fest. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Liest oder legt die relative horizontale Ausrichtung der schwebenden Tabelle fest. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Liest oder legt die relative vertikale Ausrichtung der schwebenden Tabelle fest. |
| [get_RightPadding](./get_rightpadding/)() | Liest oder legt die Menge an Abstand (in Punkten) fest, die rechts vom Inhalt von Zellen hinzugefügt wird. |
| [get_Rows](./get_rows/)() | Bietet typisierten Zugriff auf die Zeilen der Tabelle. |
| [get_Style](./get_style/)() | Liest oder legt den Tabellenstil fest, der auf diese Tabelle angewendet wird. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Liest oder legt den lokalinvarianten Stilbezeichner des Tabellenstils fest, der auf diese Tabelle angewendet wird. |
| [get_StyleName](./get_stylename/)() | Liest oder legt den Namen des Tabellenstils fest, der auf diese Tabelle angewendet wird. |
| [get_StyleOptions](./get_styleoptions/)() | Liest oder legt Bit-Flags fest, die bestimmen, wie ein Tabellenstil auf diese Tabelle angewendet wird. |
| [get_TextWrapping](./get_textwrapping/)() | Liest oder legt [TextWrapping](./get_textwrapping/) für die Tabelle fest. |
| [get_Title](./get_title/)() | Liest oder legt den Titel dieser Tabelle fest. Er liefert eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [get_TopPadding](./get_toppadding/)() | Liest oder legt die Menge an Abstand (in Punkten) fest, die über dem Inhalt von Zellen hinzugefügt wird. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Liest das Basisobjekt, von dem die vertikale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert ist [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Gibt den N-ten Kindknoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bietet Unterstützung für die foreach-artige Iteration über die Kindknoten dieses Knotens. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle Kindknoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle [SmartTag](../../aspose.words.markup/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Wählt das erste [Node](../../aspose.words/node/), das dem XPath-Ausdruck entspricht. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | Setter für [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/). |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | Setter für [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Setter für [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/). |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | Setter für [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/). |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | Setter für [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/). |
| [set_Bidi](./set_bidi/)(bool) | Setter für [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/). |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter für [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/). |
| [set_CellSpacing](./set_cellspacing/)(double) | Setter für [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Setter für [Aspose::Words::Tables::Table::get_Description](./get_description/). |
| [set_DistanceBottom](./set_distancebottom/)(double) | Setter für [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/). |
| [set_DistanceLeft](./set_distanceleft/)(double) | Setter für [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/). |
| [set_DistanceRight](./set_distanceright/)(double) | Setter für [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/). |
| [set_DistanceTop](./set_distancetop/)(double) | Setter für [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/). |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Setter für [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/). |
| [set_LeftIndent](./set_leftindent/)(double) | Setter für [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter für [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Setter für [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter für [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/). |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Setter für [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter für [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Setter für [Aspose::Words::Tables::Table::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Setter für [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Setter für [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/). |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | Setter für [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/). |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | Setter für [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/). |
| [set_Title](./set_title/)(const System::String\&) | Setter für [Aspose::Words::Tables::Table::get_Title](./get_title/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter für [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Setter für [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/). |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Setzt den angegebenen Tabellenrand auf den angegebenen Linienstil, die Breite und die Farbe. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Setzt alle Tabellenränder auf den angegebenen Linienstil, die Breite und die Farbe. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Setzt die Schattierung auf die angegebenen Werte für die gesamte Tabelle. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initialisiert eine neue Instanz der Klasse [Table](./). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

Eine minimal gültige Tabelle muss mindestens eine [Row](../row/) enthalten.

## Beispiele



Zeigt, wie man eine formatierte 2x2‑Tabelle erstellt.
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

// Während der Erstellung der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat‑Eigenschaftswerte an
// auf die aktuelle Zeile/Zelle, in der sich der Cursor befindet, und auf alle neuen Zeilen/Zellen, die er erstellt.
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

// Zuvor hinzugefügte Zeilen und Zellen werden nicht rückwirkend von Änderungen der Formatierung des Builders beeinflusst.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


Zeigt, wie man eine Tabelle erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze haben können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Der Aufruf der Methode "EnsureMinimum" an einer Tabelle stellt sicher, dass
// die Tabelle mindestens eine Zeile, Zelle und einen Absatz hat.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Fügen Sie Text zur ersten Zelle in der ersten Zeile der Tabelle hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


Zeigt, wie man durch alle Tabellen im Dokument iteriert und den Inhalt jeder Zelle ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Wir können die Methode "ToArray" auf einer Zeilensammlung verwenden, um sie in ein Array zu klonen.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Wir können die Methode "ToArray" auf einer Zellsammlung verwenden, um sie in ein Array zu klonen.
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

## Siehe auch

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
