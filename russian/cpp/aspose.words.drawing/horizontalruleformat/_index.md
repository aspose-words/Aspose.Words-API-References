---
title: "Aspose::Words::Drawing::HorizontalRuleFormat класс"
linktitle: "HorizontalRuleFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat класс. Представляет форматирование горизонтальной линии. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Представляет форматирование горизонтального правила. Чтобы узнать больше, посетите статью документации [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Получает или задает выравнивание горизонтальной линии. |
| [get_Color](./get_color/)() | Получает или задает цвет кисти, заполняющей горизонтальную линию. |
| [get_Height](./get_height/)() | Получает или задает высоту горизонтальной линии. |
| [get_NoShade](./get_noshade/)() | Указывает наличие 3D‑теней для горизонтальной линии. Если **true**, то горизонтальная линия без 3D‑теней и используется сплошной цвет. |
| [get_WidthPercent](./get_widthpercent/)() | Получает или задает длину указанной горизонтальной линии, выраженную в процентах от ширины окна. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Сеттер для [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Сеттер для [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Сеттер для [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Сеттер для [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как вставить форму горизонтального правила и настроить её форматирование.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
