---
title: "Метод Aspose::Words::Drawing::ReflectionFormat::get_Size"
linktitle: "get_Size"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ReflectionFormat::get_Size. Получает или задает значение типа double от 0.0 до 1.0, представляющее размер отражения в процентах от отражаемого объекта. Значение по умолчанию — 0.0 в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/reflectionformat/get_size/
---
## ReflectionFormat::get_Size method


Получает или задает значение типа double от 0.0 до 1.0, представляющее размер отражения в процентах от отражаемого объекта. Значение по умолчанию равно 0.0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Size()
```


## Примеры



Показывает, как взаимодействовать с эффектом формы отражения.
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

## См. также

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
