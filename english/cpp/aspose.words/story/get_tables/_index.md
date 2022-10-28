---
title: get_Tables
second_title: Aspose.Words for C++ API Reference
description: Gets a collection of tables that are immediate children of the story.
type: docs
weight: 79
url: /cpp/aspose.words/story/get_tables/
---
## Story.get_Tables method


Gets a collection of tables that are immediate children of the story.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::Story::get_Tables()
```


## Examples




Shows how to remove the first and last rows of all tables in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

SharedPtr<TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (const auto& table : System::IterateOver(tables->LINQ_OfType<SharedPtr<Table>>()))
{
    if (table->get_FirstRow() != nullptr)
    {
        table->get_FirstRow()->Remove();
    }
    if (table->get_LastRow() != nullptr)
    {
        table->get_LastRow()->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

