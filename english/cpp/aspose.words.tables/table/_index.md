---
title: Aspose::Words::Tables::Table class
linktitle: Table
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table class. Represents a table in a Word document. To learn more, visit the Working with Tables documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.tables/table/
---
## Table class


Represents a table in a Word document. 
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class Table : public CompositeNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the table. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the table. |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Resizes the table and cells according to the specified auto fit behavior. |
| [ClearBorders](./clearborders/)() | Removes all table and cell borders on this table. |
| [ClearShading](./clearshading/)() | Removes all shading on the table. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Converts cells horizontally merged by width to cells merged by [HorizontalMerge](../cellformat/get_horizontalmerge/). |
| [EnsureMinimum](./ensureminimum/)() | If the table has no rows, creates and appends one [Row](../row/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Sets the specified table border to the specified line style, width and color. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Sets all table borders to the specified line style, width and color. |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Sets shading to the specified values on whole table. |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&) | Initializes a new instance of the [Table](./) class. |
| static [Type](./type/)() |  |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [get_Alignment](./get_alignment/)() | Specifies how an inline table is aligned in the document. |
| [get_AllowAutoFit](./get_allowautofit/)() | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | Gets or sets the "Allow spacing between cells" option. |
| [get_AllowOverlap](./get_allowoverlap/)() | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is **true**. |
| [get_Bidi](./get_bidi/)() | Gets or sets whether this is a right-to-left table. |
| [get_BottomPadding](./get_bottompadding/)() | Gets or sets the amount of space (in points) to add below the contents of cells. |
| [get_CellSpacing](./get_cellspacing/)() | Gets or sets the amount of space (in points) between the cells. |
| [get_Description](./get_description/)() | Gets or sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [get_DistanceBottom](./get_distancebottom/)() | Gets or sets distance between table bottom and the surrounding text, in points. |
| [get_DistanceLeft](./get_distanceleft/)() | Gets or sets distance between table left and the surrounding text, in points. |
| [get_DistanceRight](./get_distanceright/)() | Gets or sets distance between table right and the surrounding text, in points. |
| [get_DistanceTop](./get_distancetop/)() | Gets or sets distance between table top and the surrounding text, in points. |
| [get_FirstRow](./get_firstrow/)() | Returns the first [Row](../row/) node in the table. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [get_LastRow](./get_lastrow/)() | Returns the last [Row](../row/) node in the table. |
| [get_LeftIndent](./get_leftindent/)() | Gets or sets the value that represents the left indent of the table. |
| [get_LeftPadding](./get_leftpadding/)() | Gets or sets the amount of space (in points) to add to the left of the contents of cells. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Table](../../aspose.words/nodetype/). |
| [get_PreferredWidth](./get_preferredwidth/)() | Gets or sets the table preferred width. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Gets or sets floating table relative horizontal alignment. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Gets or sets floating table relative vertical alignment. |
| [get_RightPadding](./get_rightpadding/)() | Gets or sets the amount of space (in points) to add to the right of the contents of cells. |
| [get_Rows](./get_rows/)() | Provides typed access to the rows of the table. |
| [get_Style](./get_style/)() | Gets or sets the table style applied to this table. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Gets or sets the locale independent style identifier of the table style applied to this table. |
| [get_StyleName](./get_stylename/)() | Gets or sets the name of the table style applied to this table. |
| [get_StyleOptions](./get_styleoptions/)() | Gets or sets bit flags that specify how a table style is applied to this table. |
| [get_TextWrapping](./get_textwrapping/)() | Gets or sets [TextWrapping](./get_textwrapping/) for table. |
| [get_Title](./get_title/)() | Gets or sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [get_TopPadding](./get_toppadding/)() | Gets or sets the amount of space (in points) to add above the contents of cells. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | Sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | Sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | Specifies how an inline table is aligned in the document. |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | Sets the "Allow spacing between cells" option. |
| [set_Bidi](./set_bidi/)(bool) | Sets whether this is a right-to-left table. |
| [set_BottomPadding](./set_bottompadding/)(double) | Sets the amount of space (in points) to add below the contents of cells. |
| [set_CellSpacing](./set_cellspacing/)(double) | Sets the amount of space (in points) between the cells. |
| [set_Description](./set_description/)(const System::String \&) | Sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [set_DistanceBottom](./set_distancebottom/)(double) | Sets distance between table bottom and the surrounding text, in points. |
| [set_DistanceLeft](./set_distanceleft/)(double) | Sets distance between table left and the surrounding text, in points. |
| [set_DistanceRight](./set_distanceright/)(double) | Sets distance between table right and the surrounding text, in points. |
| [set_DistanceTop](./set_distancetop/)(double) | Sets distance between table top and the surrounding text, in points. |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [Column](../../aspose.words.drawing/relativehorizontalposition/). |
| [set_LeftIndent](./set_leftindent/)(double) | Sets the value that represents the left indent of the table. |
| [set_LeftPadding](./set_leftpadding/)(double) | Sets the amount of space (in points) to add to the left of the contents of cells. |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\> \&) | Sets the table preferred width. |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Sets floating table relative horizontal alignment. |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Sets floating table relative vertical alignment. |
| [set_RightPadding](./set_rightpadding/)(double) | Sets the amount of space (in points) to add to the right of the contents of cells. |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\> \&) | Sets the table style applied to this table. |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Sets the locale independent style identifier of the table style applied to this table. |
| [set_StyleName](./set_stylename/)(const System::String \&) | Sets the name of the table style applied to this table. |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | Sets bit flags that specify how a table style is applied to this table. |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | Sets [TextWrapping](./get_textwrapping/) for table. |
| [set_Title](./set_title/)(const System::String \&) | Sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [set_TopPadding](./set_toppadding/)(double) | Sets the amount of space (in points) to add above the contents of cells. |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [Margin](../../aspose.words.drawing/relativeverticalposition/). |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/compositenode/gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [Is](../../aspose.words/compositenode/is/)(const System::TypeInfo \&) const override |  |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| static [Type](../../aspose.words/compositenode/type/)() |  |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/node/gettype/)() const override |  |
| [Is](../../aspose.words/node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../../aspose.words/node/type/)() |  |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
## Remarks


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

A minimal valid table needs to have at least one [Row](../row/).
## Examples


Shows how to build a formatted 2x2 table.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
ASSERT_EQ(CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

Shows how to create a table.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tables contain rows, which contain cells, which may have paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row, cell, and paragraph.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Add text to the first cell in the first row of the table.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

Shows how to iterate through all tables in the document and print the contents of each cell.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // We can use the "ToArray" method on a row collection to clone it into an array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // We can use the "ToArray" method on a cell collection to clone it into an array.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```
## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
