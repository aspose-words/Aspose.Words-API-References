---
title: Aspose::Words::Tables::Table::Table constructor
linktitle: Table
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::Table constructor. Initializes a new instance of the Table class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Initializes a new instance of the [Table](../) class.

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Table](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [Table](../) to the document use [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the story where you want the table inserted.

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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
