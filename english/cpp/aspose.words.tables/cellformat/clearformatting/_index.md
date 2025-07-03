---
title: Aspose::Words::Tables::CellFormat::ClearFormatting method
linktitle: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat::ClearFormatting method. Resets to default cell formatting. Does not change the width of the cell in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


Resets to default cell formatting. Does not change the width of the cell.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
```


## Examples



Shows how to combine the rows from two tables into one. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Append all rows from the current table to the next.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Remove the empty table container.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## See Also

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
