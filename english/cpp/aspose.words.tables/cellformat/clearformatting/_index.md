---
title: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: Resets to default cell formatting. Does not change the width of the cell.
type: docs
weight: 1
url: /cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method


Resets to default cell formatting. Does not change the width of the cell.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
```


## Examples




Shows how to combine the rows from two tables into one. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
SharedPtr<Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::DynamicCast<Table>(doc->GetChild(NodeType::Table, 1, true));

// Append all rows from the current table to the next.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Remove the empty table container.
secondTable->Remove();

doc->Save(ArtifactsDir + u"Table.CombineTables.docx");
```

