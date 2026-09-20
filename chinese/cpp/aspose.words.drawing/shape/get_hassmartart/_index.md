---
title: "Aspose::Words::Drawing::Shape::get_HasSmartArt 方法"
linktitle: "get_HasSmartArt"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape::get_HasSmartArt 方法。如果此 Shape 拥有 SmartArt 对象，则返回 true，在 C++ 中。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing/shape/get_hassmartart/
---
## Shape::get_HasSmartArt method


如果此 [Shape](../) 拥有 SmartArt 对象，则返回 **true**。

```cpp
bool Aspose::Words::Drawing::Shape::get_HasSmartArt()
```


## 示例



展示如何统计文档中包含 SmartArt 对象的形状数量。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"SmartArt.docx");

int32_t numberOfSmartArtShapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> shape)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> shape) -> bool
{
    return shape->get_HasSmartArt();
})));

ASSERT_EQ(2, numberOfSmartArtShapes);
```

## 另见

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
