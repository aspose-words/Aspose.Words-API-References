---
title: "Aspose::Words::Drawing::ShadowFormat класс"
linktitle: "ShadowFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShadowFormat класс. Представляет форматирование тени для объекта. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Представляет форматирование тени для объекта. Чтобы узнать больше, посетите статью документации [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) .

```cpp
class ShadowFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Очищает формат тени. |
| [get_Color](./get_color/)() | Получает или задает объект **Color**, который представляет цвет тени. Значение по умолчанию — **Black**. |
| [get_Transparency](./get_transparency/)() | Получает или задает степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0. |
| [get_Type](./get_type/)() | Получает или задает указанный [ShadowType](../shadowtype/) для [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Возвращает **true**, если форматирование, применённое к этому экземпляру, видно. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Сеттер для [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Сеттер для [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как получить цвет тени.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
