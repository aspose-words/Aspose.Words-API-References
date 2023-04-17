---
title: Aspose::Words::Tables::Table::get_Title method
linktitle: get_Title
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_Title method. Gets or sets title of this table. It provides an alternative text representation of the information contained in the table in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words.tables/table/get_title/
---
## Table::get_Title method


Gets or sets title of this table. It provides an alternative text representation of the information contained in the table.

```cpp
System::String Aspose::Words::Tables::Table::get_Title()
```

## Remarks


The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ([OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

## Examples



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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
