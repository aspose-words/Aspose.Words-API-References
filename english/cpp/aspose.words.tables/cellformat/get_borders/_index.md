---
title: Aspose::Words::Tables::CellFormat::get_Borders method
linktitle: get_Borders
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat::get_Borders method. Gets collection of borders of the cell in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.tables/cellformat/get_borders/
---
## CellFormat::get_Borders method


Gets collection of borders of the cell.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::Tables::CellFormat::get_Borders()
```


## Examples



Shows how to combine the rows from two tables into one. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
SharedPtr<Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::ExplicitCast<Table>(doc->GetChild(NodeType::Table, 1, true));

// Append all rows from the current table to the next.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Remove the empty table container.
secondTable->Remove();

doc->Save(ArtifactsDir + u"Table.CombineTables.docx");
```

## See Also

* Class [BorderCollection](../../../aspose.words/bordercollection/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
