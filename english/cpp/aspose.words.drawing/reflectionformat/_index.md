---
title: Aspose::Words::Drawing::ReflectionFormat class
linktitle: ReflectionFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ReflectionFormat class. Represents the reflection formatting for an object in C++.'
type: docs
weight: 9500
url: /cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Represents the reflection formatting for an object.

```cpp
class ReflectionFormat : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Blur](./get_blur/)() | Gets or sets a double value that specifies the degree of blur effect applied to the reflection effect in points. The default value is 0.0. |
| [get_Distance](./get_distance/)() | Gets or sets a double value that specifies the amount of separation of the reflected image from the object in points. The default value is 0.0. |
| [get_Size](./get_size/)() | Gets or sets a double value between 0.0 and 1.0 representing the size of the reflection as a percentage of the reflected object. The default value is 0.0. |
| [get_Transparency](./get_transparency/)() | Gets or sets a double value between 0.0 (opaque) and 1.0 (clear) representing the degree of transparency for the reflection effect. The default value is 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes [ReflectionFormat](./) from the parent object. |
| [set_Blur](./set_blur/)(double) | Setter for [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Setter for [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Setter for [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Setter for [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Remarks


Use the [Reflection](../shapebase/get_reflection/) property to access reflection properties of an object. You do not create instances of the [ReflectionFormat](./) class directly.

## Examples



Shows how to interact with reflection shape effect. 
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

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
