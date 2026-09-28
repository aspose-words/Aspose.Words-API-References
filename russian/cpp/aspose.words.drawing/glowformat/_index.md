---
title: "Aspose::Words::Drawing::GlowFormat класс"
linktitle: "GlowFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::GlowFormat класс. Представляет форматирование свечения для объекта в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Представляет форматирование свечения для объекта.

```cpp
class GlowFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Color](./get_color/)() | Получает или задает объект **Color**, который представляет цвет эффекта свечения. Значение по умолчанию — **Black**. |
| [get_Radius](./get_radius/)() | Получает или задает значение типа double, которое представляет длину радиуса эффекта свечения в пунктах (pt). Значение по умолчанию — 0.0. |
| [get_Transparency](./get_transparency/)() | Получает или задает степень прозрачности эффекта свечения как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет [GlowFormat](./) из родительского объекта. |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Сеттер для [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Сеттер для [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [Glow](../shapebase/get_glow/) для доступа к свойствам свечения объекта. Вы не создаёте экземпляры класса [GlowFormat](./) напрямую.

## Примеры



Показывает, как взаимодействовать с эффектом свечения формы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
