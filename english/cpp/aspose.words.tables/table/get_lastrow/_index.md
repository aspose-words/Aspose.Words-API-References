---
title: Aspose::Words::Tables::Table::get_LastRow method
linktitle: get_LastRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_LastRow method. Returns the last Row node in the table in C++.'
type: docs
weight: 88000
url: /cpp/aspose.words.tables/table/get_lastrow/
---
## Table::get_LastRow method


Returns the last [Row](../../row/) node in the table.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Table::get_LastRow()
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
## See Also

* Class [Row](../../row/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
