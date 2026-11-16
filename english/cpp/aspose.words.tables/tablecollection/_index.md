---
title: Aspose::Words::Tables::TableCollection class
linktitle: TableCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::TableCollection class. Provides typed access to a collection of Table nodes. To learn more, visit the Working with Tables documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Provides typed access to a collection of [Table](../table/) nodes. 
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class TableCollection : public NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [ToArray](./toarray/)() | Copies all tables from the collection to a new array of tables. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Table](../table/) at the given index. |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Determines whether a node is in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Copies all nodes from the collection to a new array of nodes. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [idx_get](../../aspose.words/nodecollection/idx_get/)(int32_t) | Retrieves a node at the given index. |
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

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
