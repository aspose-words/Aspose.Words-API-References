---
title: Aspose::Words::Tables::Table::get_LastRow method
linktitle: get_LastRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_LastRow method. Returns the last Row node in the table in C++.'
type: docs
weight: 25000
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
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

## See Also

* Class [Row](../../row/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
