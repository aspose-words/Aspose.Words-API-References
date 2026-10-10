---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap 方法"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap 方法。获取或设置一个值，以指定此形状是否可以在 C++ 中与其他形状重叠。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


获取或设置指定此形状是否可以覆盖其他形状的值。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## 备注


此属性影响 Microsoft Word 中形状的行为。Aspose.Words 会忽略此属性的值。

此属性仅适用于顶层形状。

默认值为 **true**。

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
