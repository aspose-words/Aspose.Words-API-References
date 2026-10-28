---
title: Aspose::Words::Tables::Row::get_NextRow method
linktitle: get_NextRow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Row::get_NextRow method. Gets the next Row node in C++.'
type: docs
weight: 15645
url: /cpp/aspose.words.tables/row/get_nextrow/
---
## Row::get_NextRow method


Gets the next [Row](../) node.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::Row::get_NextRow()
```

## Remarks

 The method can be used when you need to have typed access to table rows. If a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node is found in a table instead of a row, it is automatically traversed to get a row contained within. 
## Examples


Shows how to enumerate through all table cells.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Tables.docx"));
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Enumerate through all cells of the table.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```
## See Also

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
