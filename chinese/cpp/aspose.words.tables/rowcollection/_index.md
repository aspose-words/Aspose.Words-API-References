---
title: "Aspose::Words::Tables::RowCollection 类"
linktitle: "RowCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RowCollection 类。提供对 Row 节点集合的类型化访问。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.tables/rowcollection/
---
## RowCollection class


提供对 [Row](../row/) 节点集合的类型化访问。欲了解更多，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class RowCollection : public Aspose::Words::NodeCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 在集合的末尾添加一个节点。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中移除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 确定节点是否在集合中。 |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | 获取集合中节点的数量。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | 提供对节点集合的简单 "foreach" 样式迭代。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 检索给定索引处的 [Row](../row/)。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](./toarray/)() | 将集合中的所有行复制到一个新的行数组中。 |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
