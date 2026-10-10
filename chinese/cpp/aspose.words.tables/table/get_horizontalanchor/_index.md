---
title: "Aspose::Words::Tables::Table::get_HorizontalAnchor 方法"
linktitle: "get_HorizontalAnchor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_HorizontalAnchor 方法。获取用于计算浮动表水平定位的基对象。默认值在 C++ 中为 Column。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


获取用于计算浮动表水平定位的基对象。默认值为 [Column](../../../aspose.words.drawing/relativehorizontalposition/)。

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
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

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
