---
title: "Aspose::Words::Tables::Table::get_Rows method"
linktitle: "get_Rows"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_Rows 方法。提供在 C++ 中对表格行的类型化访问。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.tables/table/get_rows/
---
## Table::get_Rows method


提供对表格行的强类型访问。

```cpp
System::SharedPtr<Aspose::Words::Tables::RowCollection> Aspose::Words::Tables::Table::get_Rows()
```


## 示例



展示如何遍历文档中的所有表格并打印每个单元格的内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // 我们可以在行集合上使用 "ToArray" 方法将其克隆为数组。
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // 我们可以在单元格集合上使用 "ToArray" 方法将其克隆为数组。
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```


展示如何将两个表的行合并为一个。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// 下面是从文档中获取表的两种方法。
// 1 -  来自 Body 节点的 "Tables" 集合：
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - 使用 "GetChild" 方法：
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// 将当前表格的所有行追加到下一个表格。
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// 移除空的表格容器。
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## 另见

* Class [RowCollection](../../rowcollection/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
