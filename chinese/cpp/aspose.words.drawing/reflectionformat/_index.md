---
title: "Aspose::Words::Drawing::ReflectionFormat class"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ReflectionFormat class. 表示 C++ 中对象的反射格式设置。"
type: docs
weight: 9500
url: /zh/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


表示对象的反射格式。

```cpp
class ReflectionFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Blur](./get_blur/)() | 获取或设置一个 double 值，指定以点为单位应用于反射效果的模糊程度。默认值为 0.0。 |
| [get_Distance](./get_distance/)() | 获取或设置一个 double 值，指定以点为单位的反射图像与对象之间的分离量。默认值为 0.0。 |
| [get_Size](./get_size/)() | 获取或设置一个 double 值，范围在 0.0 到 1.0 之间，表示反射大小，占反射对象的百分比。默认值为 0.0。 |
| [get_Transparency](./get_transparency/)() | 获取或设置一个 double 值，范围在 0.0（不透明）到 1.0（透明）之间，表示反射效果的透明度。默认值为 0.0。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从父对象中移除 [ReflectionFormat](./)。 |
| [set_Blur](./set_blur/)(double) | 设置 [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/) 的值。 |
| [set_Distance](./set_distance/)(double) | 设置 [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/) 的值。 |
| [set_Size](./set_size/)(double) | 设置 [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/) 的值。 |
| [set_Transparency](./set_transparency/)(double) | 设置 [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/) 的值。 |
| static [Type](./type/)() |  |
## 备注


使用 [Reflection](../shapebase/get_reflection/) 属性来访问对象的反射属性。您不能直接创建 [ReflectionFormat](./) 类的实例。

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
