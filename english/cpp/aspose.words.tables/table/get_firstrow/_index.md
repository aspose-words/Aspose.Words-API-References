---
title: Aspose::Words::Tables::Table::get_FirstRow method
linktitle: get_FirstRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_FirstRow method. Returns the first Row node in the table in C++.'
type: docs
weight: 86000
url: /cpp/aspose.words.tables/table/get_firstrow/
---
## Table::get_FirstRow method


Returns the first [Row](../../row/) node in the table.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Table::get_FirstRow()
```

## Examples


Shows how to remove the first and last rows of all tables in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(tables->idx_get(0)->get_Rows()->get_Count(), 5);
ASSERT_EQ(tables->idx_get(1)->get_Rows()->get_Count(), 4);

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table>>()))
{
    System::SafeInvoke(table->get_FirstRow(), [&](auto&& expr){return expr->Remove();});
    System::SafeInvoke(table->get_LastRow(), [&](auto&& expr){return expr->Remove();});
}

ASSERT_EQ(tables->idx_get(0)->get_Rows()->get_Count(), 3);
ASSERT_EQ(tables->idx_get(1)->get_Rows()->get_Count(), 2);
```

Shows how to combine the rows from two tables into one.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(NodeType::Table, 1, true));

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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
