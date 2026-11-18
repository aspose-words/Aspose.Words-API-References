---
title: Aspose::Words::Story::get_Tables method
linktitle: get_Tables
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Story::get_Tables method. Gets a collection of tables that are immediate children of the story in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/story/get_tables/
---
## Story::get_Tables method


Gets a collection of tables that are immediate children of the story.

```cpp
System::SharedPtr<Aspose::Words::Tables::TableCollection> Aspose::Words::Story::get_Tables() override
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

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
