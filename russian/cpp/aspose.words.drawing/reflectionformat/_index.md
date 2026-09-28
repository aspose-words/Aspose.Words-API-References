---
title: "Aspose::Words::Drawing::ReflectionFormat класс"
linktitle: "ReflectionFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ReflectionFormat класс. Представляет форматирование отражения для объекта в C++."
type: docs
weight: 9500
url: /ru/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Представляет форматирование отражения для объекта.

```cpp
class ReflectionFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Blur](./get_blur/)() | Получает или задает значение типа double, которое указывает степень размытия, применяемого к эффекту отражения, в пунктах. Значение по умолчанию равно 0.0. |
| [get_Distance](./get_distance/)() | Получает или задает значение типа double, которое указывает величину отделения отражённого изображения от объекта, в пунктах. Значение по умолчанию равно 0.0. |
| [get_Size](./get_size/)() | Получает или задает значение типа double от 0.0 до 1.0, представляющее размер отражения в процентах от отражаемого объекта. Значение по умолчанию равно 0.0. |
| [get_Transparency](./get_transparency/)() | Получает или задает значение типа double от 0.0 (непрозрачный) до 1.0 (прозрачный), представляющее степень прозрачности эффекта отражения. Значение по умолчанию равно 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет [ReflectionFormat](./) из родительского объекта. |
| [set_Blur](./set_blur/)(double) | Сеттер для [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Сеттер для [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Сеттер для [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Сеттер для [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [Reflection](../shapebase/get_reflection/) для доступа к свойствам отражения объекта. Вы не создаёте экземпляры класса [ReflectionFormat](./) напрямую.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
