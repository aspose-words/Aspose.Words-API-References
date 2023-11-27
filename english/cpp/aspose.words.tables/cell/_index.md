---
title: Aspose::Words::Tables::Cell class
linktitle: Cell
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Cell class. Represents a table cell. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.tables/cell/
---
## Cell class


Represents a table cell. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class Cell : public Aspose::Words::CompositeNode,
             public Aspose::Words::ICellAttrSource,
             public Aspose::Words::Revisions::ITrackableNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Cell](./cell/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initializes a new instance of the [Cell](./) class. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [EnsureMinimum](./ensureminimum/)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [get_CellFormat](./get_cellformat/)() | Provides access to the formatting properties of the cell. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstParagraph](./get_firstparagraph/)() | Gets the first paragraph among the immediate children. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_IsFirstCell](./get_isfirstcell/)() | True if this is the first cell inside a row; false otherwise. |
| [get_IsLastCell](./get_islastcell/)() | True if this is the last cell inside a row; false otherwise. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastParagraph](./get_lastparagraph/)() | Gets the last paragraph among the immediate children. |
| [get_NextCell](./get_nextcell/)() | Gets the next [Cell](./) node. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Cell](../../aspose.words/nodetype/). |
| [get_Paragraphs](./get_paragraphs/)() | Gets a collection of paragraphs that are immediate children of the cell. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentRow](./get_parentrow/)() | Returns the parent row of the cell. |
| [get_PreviousCell](./get_previouscell/)() | Gets the previous [Cell](./) node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [get_Tables](./get_tables/)() | Gets a collection of tables that are immediate children of the cell. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


[Cell](./) can only be a child of a [Row](../row/).

[Cell](./) can contain block-level nodes [Paragraph](../../aspose.words/paragraph/) and [Table](../table/).

A minimal valid cell needs to have at least one [Paragraph](../../aspose.words/paragraph/).

## Examples



Shows how to create a table. 
```cpp
auto doc = MakeObject<Document>();
auto table = MakeObject<Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild(table);

// Tables contain rows, which contain cells, which may have paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row, cell, and paragraph.
auto firstRow = MakeObject<Row>(doc);
table->AppendChild(firstRow);

auto firstCell = MakeObject<Cell>(doc);
firstRow->AppendChild(firstCell);

auto paragraph = MakeObject<Paragraph>(doc);
firstCell->AppendChild(paragraph);

// Add text to the first call in the first row of the table.
auto run = MakeObject<Run>(doc, u"Hello world!");
paragraph->AppendChild(run);

doc->Save(ArtifactsDir + u"Table.CreateTable.docx");
```


Shows how to iterate through all tables in the document and print the contents of each cell. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");
SharedPtr<TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int i = 0; i < tables->get_Count(); i++)
{
    std::cout << "Start of Table " << i << std::endl;

    SharedPtr<RowCollection> rows = tables->idx_get(i)->get_Rows();

    // We can use the "ToArray" method on a row collection to clone it into an array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int j = 0; j < rows->get_Count(); j++)
    {
        std::cout << "\tStart of Row " << j << std::endl;

        SharedPtr<CellCollection> cells = rows->idx_get(j)->get_Cells();

        // We can use the "ToArray" method on a cell collection to clone it into an array.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int k = 0; k < cells->get_Count(); k++)
        {
            String cellText = cells->idx_get(k)->ToString(SaveFormat::Text).Trim();
            std::cout << "\t\tContents of Cell:" << k << " = \"" << cellText << "\"" << std::endl;
        }

        std::cout << "\tEnd of Row " << j << std::endl;
    }

    std::cout << "End of Table " << i << "\n" << std::endl;
}
```


Shows how to build a nested table without using a document builder. 
```cpp
void CreateNestedTable()
{
    auto doc = MakeObject<Document>();

    // Create the outer table with three rows and four columns, and then add it to the document.
    SharedPtr<Table> outerTable = CreateTable(doc, 3, 4, u"Outer Table");
    doc->get_FirstSection()->get_Body()->AppendChild(outerTable);

    // Create another table with two rows and two columns and then insert it into the first table's first cell.
    SharedPtr<Table> innerTable = CreateTable(doc, 2, 2, u"Inner Table");
    outerTable->get_FirstRow()->get_FirstCell()->AppendChild(innerTable);

    doc->Save(ArtifactsDir + u"Table.CreateNestedTable.docx");
}

static SharedPtr<Table> CreateTable(SharedPtr<Document> doc, int rowCount, int cellCount, String cellText)
{
    auto table = MakeObject<Table>(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        auto row = MakeObject<Row>(doc);
        table->AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            auto cell = MakeObject<Cell>(doc);
            cell->AppendChild(MakeObject<Paragraph>(doc));
            cell->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, cellText));

            row->AppendChild(cell);
        }
    }

    // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
    // The table must have at least one row before we can use these properties.
    // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
    // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
    table->set_Title(u"Aspose table title");
    table->set_Description(u"Aspose table description");

    return table;
}
```

## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
