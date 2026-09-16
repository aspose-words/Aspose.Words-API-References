---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel 方法"
linktitle: "get_IsTopLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel 方法。返回 true，如果此形状不是组形状的子形状（C++）。"
type: docs
weight: 36000
url: /zh/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


如果此形状不是组形状的子形状，则返回 **true**。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## 示例



展示如何判断形状是否是组形状的一部分。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// 默认情况下，形状不属于任何组形状，因此其 "IsTopLevel" 属性被设置为 "true"。
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// 一旦我们将形状合并到组形状中，"IsTopLevel" 属性会变为 "false"。
ASSERT_FALSE(shape->get_IsTopLevel());
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
