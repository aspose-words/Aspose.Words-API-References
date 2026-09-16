---
title: "Aspose::Words::Tables::Cell::get_PreviousCell 方法"
linktitle: "get_PreviousCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::get_PreviousCell 方法。获取 C++ 中的前一个 Cell 节点。"
type: docs
weight: 12500
url: /zh/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


获取前一个 [Cell](../) 节点。

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## 示例



展示如何遍历所有表格单元格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 遍历表格的所有单元格。
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## 另见

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
