---
title: "Aspose::Words::Drawing::WrapSide 枚举"
linktitle: "WrapSide"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::WrapSide 枚举。指定在 C++ 中文本环绕形状或图片的哪一侧（或多侧）。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words.drawing/wrapside/
---
## WrapSide enum


指定文本环绕形状或图片的哪一侧（或哪些侧）。

```cpp
enum class WrapSide
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Both | 0 | 文档文本在形状的两侧环绕。 |
| 左 | 1 | 文档文本仅在形状的左侧环绕。形状右侧有留白区域。 |
| 右 | 2 | 文档文本仅在形状的右侧环绕。形状左侧有留白区域。 |
| Largest | 3 | 文档文本在距离页面边距最远的一侧环绕形状，另一侧留下留白区域。 |
| Default | n/a | 默认值是 [Both](./)。 |


## 示例



展示如何将所有文本框形状替换为图像形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Textboxes in drawing canvas.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(3, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(1, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    if (shape->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox)
    {
        auto replacementShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
        replacementShape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");
        replacementShape->set_Left(shape->get_Left());
        replacementShape->set_Top(shape->get_Top());
        replacementShape->set_Width(shape->get_Width());
        replacementShape->set_Height(shape->get_Height());
        replacementShape->set_RelativeHorizontalPosition(shape->get_RelativeHorizontalPosition());
        replacementShape->set_RelativeVerticalPosition(shape->get_RelativeVerticalPosition());
        replacementShape->set_HorizontalAlignment(shape->get_HorizontalAlignment());
        replacementShape->set_VerticalAlignment(shape->get_VerticalAlignment());
        replacementShape->set_WrapType(shape->get_WrapType());
        replacementShape->set_WrapSide(shape->get_WrapSide());

        shape->get_ParentNode()->InsertAfter<System::SharedPtr<Aspose::Words::Drawing::Shape>>(replacementShape, shape);
        shape->Remove();
    }
}

shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(0, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(4, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

doc->Save(get_ArtifactsDir() + u"Shape.ReplaceTextboxesWithImages.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
