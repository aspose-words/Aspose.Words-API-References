---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height метод"
linktitle: "get_Height"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height метод. Получает или задает высоту горизонтальной линии в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Получает или задает высоту горизонтальной линии.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Примечания


Это сокращение к свойству [Height](../../shapebase/get_height/).

Допустимые значения находятся в диапазоне от 0 до 1584 включительно.

Значение по умолчанию — 1.5.

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

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
