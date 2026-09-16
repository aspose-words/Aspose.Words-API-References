---
title: "Aspose::Words::Tables::Table::get_AllowOverlap 方法"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_AllowOverlap 方法。获取浮动表在显示时是否允许文档中的其他浮动对象覆盖其范围。默认值在 C++ 中为 true。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


获取浮动表格在显示时是否允许文档中的其他浮动对象覆盖其范围。默认值为 **true**。

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
```


## 示例



展示如何使用浮动表格属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // 在 RelativeHorizontalPosition 中，HorizontalAnchor setter 仅支持 Margin、Page、Column。
    // 对于任何其他值，将抛出 ArgumentException。
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // 在 RelativeVerticalPosition 中，VerticalAnchor setter 仅支持 Margin、Page、Paragraph。
    // 对于任何其他值，将抛出 ArgumentException。
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
