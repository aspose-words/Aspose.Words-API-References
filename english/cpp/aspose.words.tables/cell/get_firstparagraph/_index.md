---
title: get_FirstParagraph
second_title: Aspose.Words for C++ API Reference
description: Gets the first paragraph among the immediate children.
type: docs
weight: 66
url: /cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Gets the first paragraph among the immediate children.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Examples



Shows how to create a nested table using a document builder. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Build the outer table.
SharedPtr<Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Move to the first cell of the outer table, the build another table inside the cell.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertNestedTable.docx");
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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
