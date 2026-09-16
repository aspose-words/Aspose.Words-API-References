---
title: "Aspose::Words::Drawing::ReflectionFormat::get_Distance 方法"
linktitle: "get_Distance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ReflectionFormat::get_Distance 方法。获取或设置一个 double 值，指定以点为单位的反射图像与对象之间的分离距离。默认值在 C++ 中为 0.0。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/reflectionformat/get_distance/
---
## ReflectionFormat::get_Distance method


获取或设置一个 double 值，指定以点为单位的反射图像与对象之间的分离量。默认值为 0.0。

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Distance()
```


## 示例



展示如何与反射形状效果交互。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## 另见

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
