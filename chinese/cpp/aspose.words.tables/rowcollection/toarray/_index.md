---
title: "Aspose::Words::Tables::RowCollection::ToArray 方法"
linktitle: "ToArray"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::RowCollection::ToArray 方法。将集合中的所有行复制到 C++ 中的新行数组。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.tables/rowcollection/toarray/
---
## RowCollection::ToArray method


将集合中的所有行复制到一个新的行数组中。

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Tables::Row>> Aspose::Words::Tables::RowCollection::ToArray()
```


### ReturnValue

一个行数组。

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

## 另见

* Class [Row](../../row/)
* Class [RowCollection](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
